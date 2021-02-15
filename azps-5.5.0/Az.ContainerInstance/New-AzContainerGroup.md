---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/new-azcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/New-AzContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/New-AzContainerGroup.md
ms.openlocfilehash: 20daa8d14f77ca4563c072d58d1c2269235cb164
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112093"
---
# <span data-ttu-id="13a5c-101">New-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="13a5c-101">New-AzContainerGroup</span></span>

## <span data-ttu-id="13a5c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="13a5c-102">SYNOPSIS</span></span>
<span data-ttu-id="13a5c-103">Cria um grupo de contêineres.</span><span class="sxs-lookup"><span data-stu-id="13a5c-103">Creates a container group.</span></span>

## <span data-ttu-id="13a5c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="13a5c-104">SYNTAX</span></span>

### <span data-ttu-id="13a5c-105">CreateContainerGroupBaseParamSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="13a5c-105">CreateContainerGroupBaseParamSet (Default)</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] [-Location <String>] [-AssignIdentity] [-OsType <String>]
 [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>]
 [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>] [-EnvironmentVariable <Hashtable>]
 [-RegistryServerDomain <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13a5c-106">CreateContainerGroupWithAzureFileMountParamSet</span><span class="sxs-lookup"><span data-stu-id="13a5c-106">CreateContainerGroupWithAzureFileMountParamSet</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] -AzureFileVolumeShareName <String>
 -AzureFileVolumeAccountCredential <PSCredential> -AzureFileVolumeMountPath <String> [-Location <String>]
 [-AssignIdentity] [-OsType <String>] [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>]
 [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>]
 [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13a5c-107">CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet</span><span class="sxs-lookup"><span data-stu-id="13a5c-107">CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] -AzureFileVolumeShareName <String>
 -AzureFileVolumeAccountCredential <PSCredential> -AzureFileVolumeMountPath <String> [-Location <String>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsType <String>] [-RestartPolicy <String>]
 [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>]
 [-Command <String>] [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13a5c-108">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="13a5c-108">ExplicitIdentityParameterSet</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] [-Location <String>] -IdentityType <ResourceIdentityType>
 [-IdentityId <String[]>] [-OsType <String>] [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>]
 [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>]
 [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13a5c-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="13a5c-109">DESCRIPTION</span></span>
<span data-ttu-id="13a5c-110">Os **cmdlets New-AzContainerGroup** criam um grupo de contêineres.</span><span class="sxs-lookup"><span data-stu-id="13a5c-110">The **New-AzContainerGroup** cmdlets creates a container group.</span></span>

## <span data-ttu-id="13a5c-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="13a5c-111">EXAMPLES</span></span>

### <span data-ttu-id="13a5c-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="13a5c-112">Example 1</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image nginx -OsType Linux -IpAddressType Public -Port @(8000)

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {8000}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="13a5c-113">Esse comando cria um grupo de contêineres usando a imagem nginx mais recente e solicita um endereço IP público com a porta 8000 de abertura.</span><span class="sxs-lookup"><span data-stu-id="13a5c-113">This commands creates a container group using latest nginx image and requests a public IP address with opening port 8000.</span></span>

### <span data-ttu-id="13a5c-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="13a5c-114">Example 2</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image alpine -OsType Linux -Command "/bin/sh -c myscript.sh" -EnvironmentVariable @{"env1"="value1";"env2"="value2"}

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                :
Ports                    :
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="13a5c-115">Esse comando cria um grupo de contêineres e executa um script personalizado dentro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="13a5c-115">This commands creates a container group and runs a custom script inside the container.</span></span>

### <span data-ttu-id="13a5c-116">Exemplo 3: cria um grupo de contêineres de execução até a conclusão.</span><span class="sxs-lookup"><span data-stu-id="13a5c-116">Example 3: Creates a run-to-completion container group.</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image alpine -OsType Linux -Command "echo hello" -RestartPolicy Never

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                :
Ports                    :
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="13a5c-117">Esse comando cria um grupo de contêineres que imprime "olá" e para.</span><span class="sxs-lookup"><span data-stu-id="13a5c-117">This commands creates a container group which prints out 'hello' and stops.</span></span>

### <span data-ttu-id="13a5c-118">Exemplo 4: cria um grupo de contêineres usando imagem no Registro de Contêineres do Azure</span><span class="sxs-lookup"><span data-stu-id="13a5c-118">Example 4: Creates a container group using image in Azure Container Registry</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("myacr", $secpasswd)
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image myacr.azurecr.io/nginx:latest -IpAddressType Public -RegistryCredential $mycred

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials : {myacr}
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {80}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="13a5c-119">Esse comando cria um grupo de contêineres usando uma imagem nginx no Registro de Contêineres do Azure.</span><span class="sxs-lookup"><span data-stu-id="13a5c-119">This commands creates a container group using a nginx image in Azure Container Registry.</span></span>

### <span data-ttu-id="13a5c-120">Exemplo 5: cria um grupo de contêineres usando imagem no registro de imagem de contêiner personalizado</span><span class="sxs-lookup"><span data-stu-id="13a5c-120">Example 5: Creates a container group using image in custom container image registry</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("username", $secpasswd)
PS C:\> New-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer -Image myserver.com/myimage:latest -RegistryServer myserver.com -RegistryCredential $mycred

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials : {myserver.com}
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {80}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="13a5c-121">Esse comando cria um grupo de contêineres usando uma imagem personalizada de um registro de imagem de contêiner personalizado.</span><span class="sxs-lookup"><span data-stu-id="13a5c-121">This commands creates a container group using a custom image from a custom container image registry.</span></span>

### <span data-ttu-id="13a5c-122">Exemplo 6: cria um grupo de contêineres que monta o volume do Arquivo do Azure</span><span class="sxs-lookup"><span data-stu-id="13a5c-122">Example 6: Creates a container group that mounts Azure File volume</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("username", $secpasswd)
PS C:\> New-AzContainerGroup -ResourceGroupName MyResourceGroup -Name mycontainer -Image alpine -AzureFileVolumeShareName myshare -AzureFileVolumeAccountCredential $mycred -AzureFileVolumeMountPath /mnt/azfile

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials : {myserver.com}
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {80}
OsType                   : Linux
Volumes                  : {AzureFile}
State                    : Running
Events                   : {}
```

<span data-ttu-id="13a5c-123">Esse comando cria um grupo de contêineres que monta o compartilhamento de Arquivo do Azure fornecido `/mnt/azfile` para.</span><span class="sxs-lookup"><span data-stu-id="13a5c-123">This commands creates a container group that mounts the provided Azure File share to `/mnt/azfile`.</span></span>

### <span data-ttu-id="13a5c-124">Exemplo 7</span><span class="sxs-lookup"><span data-stu-id="13a5c-124">Example 7</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image nginx -OsType Linux -IpAddressType Public -Port @(8000) -AssignIdentity

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {8000}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
Identity                 : Microsoft.Azure.Management.ContainerInstance.Models.ContainerGroupIdentity
```

<span data-ttu-id="13a5c-125">Esse comando cria um grupo de contêineres com identidade atribuída pelo sistema usando a imagem nginx mais recente e solicita um endereço IP público com a porta 8000 de abertura.</span><span class="sxs-lookup"><span data-stu-id="13a5c-125">This commands creates a container group with system assigned identity using latest nginx image and requests a public IP address with opening port 8000.</span></span>

### <span data-ttu-id="13a5c-126">Exemplo 8</span><span class="sxs-lookup"><span data-stu-id="13a5c-126">Example 8</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image nginx -OsType Linux -IpAddressType Public -Port @(8000) -IdentityType SystemAssignedUserAssigned -IdentityId /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.ManagedIdentity/userAssignedIdentities/<UserIdentityName>

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {8000}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
Identity                 : Microsoft.Azure.Management.ContainerInstance.Models.ContainerGroupIdentity
```

<span data-ttu-id="13a5c-127">Esse comando cria um grupo de contêineres com o sistema atribuído e a identidade atribuída pelo usuário usando a imagem nginx mais recente e solicita um endereço IP público com a porta 8000 de abertura.</span><span class="sxs-lookup"><span data-stu-id="13a5c-127">This commands creates a container group with system assigned and user assigned identity using latest nginx image and requests a public IP address with opening port 8000.</span></span>

## <span data-ttu-id="13a5c-128">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="13a5c-128">PARAMETERS</span></span>

### <span data-ttu-id="13a5c-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="13a5c-129">-AssignIdentity</span></span>
<span data-ttu-id="13a5c-130">Habilitar a identidade atribuída ao sistema</span><span class="sxs-lookup"><span data-stu-id="13a5c-130">Enable system assigned identity</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateContainerGroupBaseParamSet, CreateContainerGroupWithAzureFileMountParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13a5c-131">-AzureFileVolumeAccountCredential</span><span class="sxs-lookup"><span data-stu-id="13a5c-131">-AzureFileVolumeAccountCredential</span></span>
<span data-ttu-id="13a5c-132">A credencial da conta de armazenamento do compartilhamento arquivo do Azure para ser montado onde o nome de usuário é o nome da conta de armazenamento e a chave é a chave da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="13a5c-132">The storage account credential of the Azure File share to mount where the username is the storage account name and the key is the storage account key.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet, CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13a5c-133">-AzureFileVolumeMountPath</span><span class="sxs-lookup"><span data-stu-id="13a5c-133">-AzureFileVolumeMountPath</span></span>
<span data-ttu-id="13a5c-134">O caminho de montagem para o volume do Arquivo do Azure.</span><span class="sxs-lookup"><span data-stu-id="13a5c-134">The mount path for the Azure File volume.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet, CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13a5c-135">-AzureFileVolumeShareName</span><span class="sxs-lookup"><span data-stu-id="13a5c-135">-AzureFileVolumeShareName</span></span>
<span data-ttu-id="13a5c-136">O nome do compartilhamento do Arquivo do Azure para montagem.</span><span class="sxs-lookup"><span data-stu-id="13a5c-136">The name of the Azure File share to mount.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet, CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13a5c-137">-Command</span><span class="sxs-lookup"><span data-stu-id="13a5c-137">-Command</span></span>
<span data-ttu-id="13a5c-138">O comando a ser executado no contêiner.</span><span class="sxs-lookup"><span data-stu-id="13a5c-138">The command to run in the container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13a5c-139">-Cpu</span><span class="sxs-lookup"><span data-stu-id="13a5c-139">-Cpu</span></span>
<span data-ttu-id="13a5c-140">Os núcleos de CPU necessários.</span><span class="sxs-lookup"><span data-stu-id="13a5c-140">The required CPU cores.</span></span>
<span data-ttu-id="13a5c-141">Padrão: 1</span><span class="sxs-lookup"><span data-stu-id="13a5c-141">Default: 1</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13a5c-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13a5c-142">-DefaultProfile</span></span>
<span data-ttu-id="13a5c-143">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="13a5c-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13a5c-144">-DnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="13a5c-144">-DnsNameLabel</span></span>
<span data-ttu-id="13a5c-145">O rótulo de nome DNS do endereço IP.</span><span class="sxs-lookup"><span data-stu-id="13a5c-145">The DNS name label for the IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13a5c-146">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="13a5c-146">-EnvironmentVariable</span></span>
<span data-ttu-id="13a5c-147">As variáveis de ambiente do contêiner.</span><span class="sxs-lookup"><span data-stu-id="13a5c-147">The container environment variables.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13a5c-148">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="13a5c-148">-IdentityId</span></span>
<span data-ttu-id="13a5c-149">IDs de identidade atribuídas pelo usuário</span><span class="sxs-lookup"><span data-stu-id="13a5c-149">The user assigned identity IDs</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13a5c-150">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="13a5c-150">-IdentityType</span></span>
<span data-ttu-id="13a5c-151">O tipo de identidade gerenciada</span><span class="sxs-lookup"><span data-stu-id="13a5c-151">The managed identity type</span></span>

```yaml
Type: Microsoft.Azure.Management.ContainerInstance.Models.ResourceIdentityType
Parameter Sets: CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet, ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13a5c-152">-Imagem</span><span class="sxs-lookup"><span data-stu-id="13a5c-152">-Image</span></span>
<span data-ttu-id="13a5c-153">A imagem do contêiner.</span><span class="sxs-lookup"><span data-stu-id="13a5c-153">The container image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13a5c-154">-IpAddressType</span><span class="sxs-lookup"><span data-stu-id="13a5c-154">-IpAddressType</span></span>
<span data-ttu-id="13a5c-155">O tipo de endereço IP.</span><span class="sxs-lookup"><span data-stu-id="13a5c-155">The IP address type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Public

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13a5c-156">-Local</span><span class="sxs-lookup"><span data-stu-id="13a5c-156">-Location</span></span>
<span data-ttu-id="13a5c-157">O local do grupo contêiner.</span><span class="sxs-lookup"><span data-stu-id="13a5c-157">The container group Location.</span></span>
<span data-ttu-id="13a5c-158">Padrão para o local do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="13a5c-158">Default to the location of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13a5c-159">-MemoryInGB</span><span class="sxs-lookup"><span data-stu-id="13a5c-159">-MemoryInGB</span></span>
<span data-ttu-id="13a5c-160">A memória necessária em GB.</span><span class="sxs-lookup"><span data-stu-id="13a5c-160">The required memory in GB.</span></span>
<span data-ttu-id="13a5c-161">Padrão: 1,5</span><span class="sxs-lookup"><span data-stu-id="13a5c-161">Default: 1.5</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases: Memory

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13a5c-162">-Nome</span><span class="sxs-lookup"><span data-stu-id="13a5c-162">-Name</span></span>
<span data-ttu-id="13a5c-163">O nome do grupo de contêineres.</span><span class="sxs-lookup"><span data-stu-id="13a5c-163">The container group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13a5c-164">-OsType</span><span class="sxs-lookup"><span data-stu-id="13a5c-164">-OsType</span></span>
<span data-ttu-id="13a5c-165">O tipo de sistema operacional do contêiner.</span><span class="sxs-lookup"><span data-stu-id="13a5c-165">The container OS type.</span></span>
<span data-ttu-id="13a5c-166">Padrão: Linux</span><span class="sxs-lookup"><span data-stu-id="13a5c-166">Default: Linux</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Linux, Windows

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13a5c-167">-Porta</span><span class="sxs-lookup"><span data-stu-id="13a5c-167">-Port</span></span>
<span data-ttu-id="13a5c-168">As portas para abrir.</span><span class="sxs-lookup"><span data-stu-id="13a5c-168">The port(s) to open.</span></span> <span data-ttu-id="13a5c-169">Padrão: [80]</span><span class="sxs-lookup"><span data-stu-id="13a5c-169">Default: [80]</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13a5c-170">-RegistryCredential</span><span class="sxs-lookup"><span data-stu-id="13a5c-170">-RegistryCredential</span></span>
<span data-ttu-id="13a5c-171">A credencial do registro de contêiner personalizado.</span><span class="sxs-lookup"><span data-stu-id="13a5c-171">The custom container registry credential.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13a5c-172">-RegistryServerDomain</span><span class="sxs-lookup"><span data-stu-id="13a5c-172">-RegistryServerDomain</span></span>
<span data-ttu-id="13a5c-173">O servidor de logon do registro de contêiner personalizado.</span><span class="sxs-lookup"><span data-stu-id="13a5c-173">The custom container registry login server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RegistryServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13a5c-174">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13a5c-174">-ResourceGroupName</span></span>
<span data-ttu-id="13a5c-175">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="13a5c-175">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13a5c-176">-RestartPolicy</span><span class="sxs-lookup"><span data-stu-id="13a5c-176">-RestartPolicy</span></span>
<span data-ttu-id="13a5c-177">A política de reinicialização do contêiner.</span><span class="sxs-lookup"><span data-stu-id="13a5c-177">The container restart policy.</span></span> <span data-ttu-id="13a5c-178">Padrão: Sempre</span><span class="sxs-lookup"><span data-stu-id="13a5c-178">Default: Always</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Always, Never, OnFailure

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13a5c-179">-Tag</span><span class="sxs-lookup"><span data-stu-id="13a5c-179">-Tag</span></span>
<span data-ttu-id="13a5c-180">{{Fill Tag Description}}</span><span class="sxs-lookup"><span data-stu-id="13a5c-180">{{Fill Tag Description}}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13a5c-181">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="13a5c-181">-Confirm</span></span>
<span data-ttu-id="13a5c-182">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13a5c-182">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13a5c-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13a5c-183">-WhatIf</span></span>
<span data-ttu-id="13a5c-184">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="13a5c-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13a5c-185">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="13a5c-185">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13a5c-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13a5c-186">CommonParameters</span></span>
<span data-ttu-id="13a5c-187">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13a5c-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13a5c-188">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13a5c-188">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13a5c-189">Entradas</span><span class="sxs-lookup"><span data-stu-id="13a5c-189">INPUTS</span></span>

### <span data-ttu-id="13a5c-190">System.String</span><span class="sxs-lookup"><span data-stu-id="13a5c-190">System.String</span></span>

### <span data-ttu-id="13a5c-191">System.String[]</span><span class="sxs-lookup"><span data-stu-id="13a5c-191">System.String[]</span></span>

### <span data-ttu-id="13a5c-192">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="13a5c-192">System.Collections.Hashtable</span></span>

## <span data-ttu-id="13a5c-193">Saídas</span><span class="sxs-lookup"><span data-stu-id="13a5c-193">OUTPUTS</span></span>

### <span data-ttu-id="13a5c-194">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="13a5c-194">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="13a5c-195">Notas</span><span class="sxs-lookup"><span data-stu-id="13a5c-195">NOTES</span></span>

## <span data-ttu-id="13a5c-196">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="13a5c-196">RELATED LINKS</span></span>
