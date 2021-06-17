
# Building the docs

1. In a terminal/prompt, navigate to this folder (`.../docs/`).

2. Make sure to have the requirements installed in your environment. (Also install the main project's requirements of course, if one has not already done so.)

   ```bash
   pip install -r requirements.txt
   ```

3. Clean the build directory (if there was ever anything in there to begin with).

   ```bash
   sphinx-build -M clean ./ _build/
   ```

4. Create reST files for all detected packages.

   ```bash
   sphinx-apidoc -f -o ./source/ ../pluralkit/
   ```

5. Make the docs.

   ```bash
   sphinx-build -M html ./ _build/
   ```

   The output under `.../docs/_build/html/` represents the HTML documentation.