k8s_yaml('config.yaml')

deps = listdir('src')

custom_build(
  'test',
  'docker build -t $EXPECTED_REF src',
  deps=deps,
)