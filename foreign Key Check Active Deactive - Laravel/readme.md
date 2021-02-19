<div style="margin:0 auto;display: table; text-transform:capitalize;">
<h2>How To Solve The Foreign key Check Problem Simply ??</h2>
<h3>First: Disable Foreign Key Check While Migration </h3>
<p>
	Example-1: <blockquote>DB::statement('SET FOREIGN_KEY_CHECKS=0');</blockquote>
</p>
<p>OR</p>
<p>
	Example-2:
<blockquote>Schema::disableForeignKeyConstraints();</blockquote>
</p>
<h4>Write Your Database Opretions here like 'drop Table' Then</h4>
<h3>How To Enable Foreign Key Check While Migration : Rollback ?</h3>
<p>
	Example-1: 
<blockquote>DB::statement('SET FOREIGN_KEY_CHECKS=1');</blockquote>
</p>
<p>
	Example-2:
	<blockquote>Schema::disableForeignKeyConstraints();</blockquote>
</p>
</div>