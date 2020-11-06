---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerinstance/new-azurermcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/New-AzureRmContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/New-AzureRmContainerGroup.md
ms.openlocfilehash: 1823759b72bdb3162164068732f3a8201fcfb589
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427252"
---
# <span data-ttu-id="3d54b-101">New-AzureRmContainerGroup</span><span class="sxs-lookup"><span data-stu-id="3d54b-101">New-AzureRmContainerGroup</span></span>

## <span data-ttu-id="3d54b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3d54b-102">SYNOPSIS</span></span>
<span data-ttu-id="3d54b-103">Cria um grupo de contêineres.</span><span class="sxs-lookup"><span data-stu-id="3d54b-103">Creates a container group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d54b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3d54b-104">SYNTAX</span></span>

### <span data-ttu-id="3d54b-105">CreateContainerGroupBaseParamSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="3d54b-105">CreateContainerGroupBaseParamSet (Default)</span></span>
```
New-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] [-Location <String>] [-OsType <String>] [-RestartPolicy <String>]
 [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>]
 [-Command <String>] [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d54b-106">CreateContainerGroupWithAzureFileMountParamSet</span><span class="sxs-lookup"><span data-stu-id="3d54b-106">CreateContainerGroupWithAzureFileMountParamSet</span></span>
```
New-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] -AzureFileVolumeShareName <String>
 -AzureFileVolumeAccountCredential <PSCredential> -AzureFileVolumeMountPath <String> [-Location <String>]
 [-OsType <String>] [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>]
 [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>] [-EnvironmentVariable <Hashtable>]
 [-RegistryServerDomain <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d54b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3d54b-107">DESCRIPTION</span></span>
<span data-ttu-id="3d54b-108">Os cmdlets **New-AzureRmContainerGroup** criam um grupo de contêineres.</span><span class="sxs-lookup"><span data-stu-id="3d54b-108">The **New-AzureRmContainerGroup** cmdlets creates a container group.</span></span>

## <span data-ttu-id="3d54b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3d54b-109">EXAMPLES</span></span>

### <span data-ttu-id="3d54b-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3d54b-110">Example 1</span></span>
```
PS C:\> New-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer -Image nginx -OsType Linux -IpAddressType Public -Port @(8000)

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

<span data-ttu-id="3d54b-111">Esses comandos criam um grupo de contêineres usando a imagem Nginx mais recente e solicita um endereço IP público com a porta de abertura 8000.</span><span class="sxs-lookup"><span data-stu-id="3d54b-111">This commands creates a container group using latest nginx image and requests a public IP address with opening port 8000.</span></span>

### <span data-ttu-id="3d54b-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="3d54b-112">Example 2</span></span>
```
PS C:\> New-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer -Image alpine -OsType Linux -Command "/bin/sh -c myscript.sh" -EnvironmentVariable @{"env1"="value1";"env2"="value2"}

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

<span data-ttu-id="3d54b-113">Esses comandos criam um grupo de contêineres e executam um script personalizado dentro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="3d54b-113">This commands creates a container group and runs a custom script inside the container.</span></span>

### <span data-ttu-id="3d54b-114">Exemplo 3: cria um grupo de contêiners Run-to-Completing.</span><span class="sxs-lookup"><span data-stu-id="3d54b-114">Example 3: Creates a run-to-completion container group.</span></span>
```
PS C:\> New-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer -Image alpine -OsType Linux -Command "echo hello" -RestartPolicy Never

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

<span data-ttu-id="3d54b-115">Esses comandos criam um grupo de contêineres que imprime ' Olá ' e para de parar.</span><span class="sxs-lookup"><span data-stu-id="3d54b-115">This commands creates a container group which prints out 'hello' and stops.</span></span>

### <span data-ttu-id="3d54b-116">Exemplo 4: cria um grupo de contêineres usando a imagem no registro do contêiner do Azure</span><span class="sxs-lookup"><span data-stu-id="3d54b-116">Example 4: Creates a container group using image in Azure Container Registry</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("myacr", $secpasswd)
PS C:\> New-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer -Image myacr.azurecr.io/nginx:latest -IpAddressType Public -RegistryCredential $mycred

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

<span data-ttu-id="3d54b-117">Esses comandos criam um grupo de contêineres usando uma imagem de Nginx no registro do contêiner do Azure.</span><span class="sxs-lookup"><span data-stu-id="3d54b-117">This commands creates a container group using a nginx image in Azure Container Registry.</span></span>

### <span data-ttu-id="3d54b-118">Exemplo 5: cria um grupo de contêineres usando a imagem no registro de imagem do contêiner personalizado</span><span class="sxs-lookup"><span data-stu-id="3d54b-118">Example 5: Creates a container group using image in custom container image registry</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("username", $secpasswd)
PS C:\> New-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer -Image myserver.com/myimage:latest -RegistryServer myserver.com -RegistryCredential $mycred

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

<span data-ttu-id="3d54b-119">Esses comandos criam um grupo de contêineres usando uma imagem personalizada de um registro de imagem de contêiner personalizado.</span><span class="sxs-lookup"><span data-stu-id="3d54b-119">This commands creates a container group using a custom image from a custom container image registry.</span></span>

### <span data-ttu-id="3d54b-120">Exemplo 6: cria um grupo de contêineres que monta o volume de arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="3d54b-120">Example 6: Creates a container group that mounts Azure File volume</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("username", $secpasswd)
PS C:\> New-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer -Image alpine -AzureFileVolumeShareName myshare -AzureFileVolumeAccountKey $mycred -AzureFileVolumeMountPath /mnt/azfile

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

<span data-ttu-id="3d54b-121">Esses comandos criam um grupo de contêineres que monta o compartilhamento de arquivos do Azure fornecido `/mnt/azfile` .</span><span class="sxs-lookup"><span data-stu-id="3d54b-121">This commands creates a container group that mounts the provided Azure File share to `/mnt/azfile`.</span></span>

## <span data-ttu-id="3d54b-122">OS</span><span class="sxs-lookup"><span data-stu-id="3d54b-122">PARAMETERS</span></span>

### <span data-ttu-id="3d54b-123">-AzureFileVolumeAccountCredential</span><span class="sxs-lookup"><span data-stu-id="3d54b-123">-AzureFileVolumeAccountCredential</span></span>
<span data-ttu-id="3d54b-124">A credencial da conta de armazenamento do compartilhamento de arquivos do Azure para montagem em que o nome de usuário é o nome da conta de armazenamento e a chave é a chave da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3d54b-124">The storage account credential of the Azure File share to mount where the username is the storage account name and the key is the storage account key.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d54b-125">-AzureFileVolumeMountPath</span><span class="sxs-lookup"><span data-stu-id="3d54b-125">-AzureFileVolumeMountPath</span></span>
<span data-ttu-id="3d54b-126">O caminho de montagem para o volume de arquivo do Azure.</span><span class="sxs-lookup"><span data-stu-id="3d54b-126">The mount path for the Azure File volume.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d54b-127">-AzureFileVolumeShareName</span><span class="sxs-lookup"><span data-stu-id="3d54b-127">-AzureFileVolumeShareName</span></span>
<span data-ttu-id="3d54b-128">O nome do compartilhamento de arquivos do Azure a ser montado.</span><span class="sxs-lookup"><span data-stu-id="3d54b-128">The name of the Azure File share to mount.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d54b-129">-Comando</span><span class="sxs-lookup"><span data-stu-id="3d54b-129">-Command</span></span>
<span data-ttu-id="3d54b-130">O comando a ser executado no contêiner.</span><span class="sxs-lookup"><span data-stu-id="3d54b-130">The command to run in the container.</span></span>

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

### <span data-ttu-id="3d54b-131">-CPU</span><span class="sxs-lookup"><span data-stu-id="3d54b-131">-Cpu</span></span>
<span data-ttu-id="3d54b-132">Os núcleos de CPU obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="3d54b-132">The required CPU cores.</span></span>
<span data-ttu-id="3d54b-133">Padrão: 1</span><span class="sxs-lookup"><span data-stu-id="3d54b-133">Default: 1</span></span>

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

### <span data-ttu-id="3d54b-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d54b-134">-DefaultProfile</span></span>
<span data-ttu-id="3d54b-135">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3d54b-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d54b-136">-DnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="3d54b-136">-DnsNameLabel</span></span>
<span data-ttu-id="3d54b-137">O rótulo de nome DNS para o endereço IP.</span><span class="sxs-lookup"><span data-stu-id="3d54b-137">The DNS name label for the IP address.</span></span>

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

### <span data-ttu-id="3d54b-138">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="3d54b-138">-EnvironmentVariable</span></span>
<span data-ttu-id="3d54b-139">As variáveis de ambiente do contêiner.</span><span class="sxs-lookup"><span data-stu-id="3d54b-139">The container environment variables.</span></span>

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

### <span data-ttu-id="3d54b-140">-Imagem</span><span class="sxs-lookup"><span data-stu-id="3d54b-140">-Image</span></span>
<span data-ttu-id="3d54b-141">A imagem do contêiner.</span><span class="sxs-lookup"><span data-stu-id="3d54b-141">The container image.</span></span>

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

### <span data-ttu-id="3d54b-142">-IpAddresstype</span><span class="sxs-lookup"><span data-stu-id="3d54b-142">-IpAddressType</span></span>
<span data-ttu-id="3d54b-143">O tipo de endereço IP.</span><span class="sxs-lookup"><span data-stu-id="3d54b-143">The IP address type.</span></span>

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

### <span data-ttu-id="3d54b-144">-Local</span><span class="sxs-lookup"><span data-stu-id="3d54b-144">-Location</span></span>
<span data-ttu-id="3d54b-145">O local do grupo de contêineres.</span><span class="sxs-lookup"><span data-stu-id="3d54b-145">The container group Location.</span></span>
<span data-ttu-id="3d54b-146">Padrão para o local do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3d54b-146">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="3d54b-147">-MemoryInGB</span><span class="sxs-lookup"><span data-stu-id="3d54b-147">-MemoryInGB</span></span>
<span data-ttu-id="3d54b-148">A memória necessária em GB.</span><span class="sxs-lookup"><span data-stu-id="3d54b-148">The required memory in GB.</span></span>
<span data-ttu-id="3d54b-149">Padrão: 1,5</span><span class="sxs-lookup"><span data-stu-id="3d54b-149">Default: 1.5</span></span>

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

### <span data-ttu-id="3d54b-150">-Nome</span><span class="sxs-lookup"><span data-stu-id="3d54b-150">-Name</span></span>
<span data-ttu-id="3d54b-151">O nome do grupo de contêineres.</span><span class="sxs-lookup"><span data-stu-id="3d54b-151">The container group name.</span></span>

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

### <span data-ttu-id="3d54b-152">-OsType</span><span class="sxs-lookup"><span data-stu-id="3d54b-152">-OsType</span></span>
<span data-ttu-id="3d54b-153">O tipo de sistema operacional do contêiner.</span><span class="sxs-lookup"><span data-stu-id="3d54b-153">The container OS type.</span></span>
<span data-ttu-id="3d54b-154">Padrão: Linux</span><span class="sxs-lookup"><span data-stu-id="3d54b-154">Default: Linux</span></span>

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

### <span data-ttu-id="3d54b-155">-Porta</span><span class="sxs-lookup"><span data-stu-id="3d54b-155">-Port</span></span>
<span data-ttu-id="3d54b-156">A (s) porta (s) para abrir.</span><span class="sxs-lookup"><span data-stu-id="3d54b-156">The port(s) to open.</span></span> <span data-ttu-id="3d54b-157">Padrão: [80]</span><span class="sxs-lookup"><span data-stu-id="3d54b-157">Default: [80]</span></span>

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

### <span data-ttu-id="3d54b-158">-RegistryCredential</span><span class="sxs-lookup"><span data-stu-id="3d54b-158">-RegistryCredential</span></span>
<span data-ttu-id="3d54b-159">A credencial personalizada do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="3d54b-159">The custom container registry credential.</span></span>

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

### <span data-ttu-id="3d54b-160">-RegistryServerDomain</span><span class="sxs-lookup"><span data-stu-id="3d54b-160">-RegistryServerDomain</span></span>
<span data-ttu-id="3d54b-161">O servidor de logon do contêiner de contêiner personalizado.</span><span class="sxs-lookup"><span data-stu-id="3d54b-161">The custom container registry login server.</span></span>

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

### <span data-ttu-id="3d54b-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d54b-162">-ResourceGroupName</span></span>
<span data-ttu-id="3d54b-163">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3d54b-163">The resource group name.</span></span>

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

### <span data-ttu-id="3d54b-164">-RestartPolicy</span><span class="sxs-lookup"><span data-stu-id="3d54b-164">-RestartPolicy</span></span>
<span data-ttu-id="3d54b-165">A política de reinicialização do contêiner.</span><span class="sxs-lookup"><span data-stu-id="3d54b-165">The container restart policy.</span></span> <span data-ttu-id="3d54b-166">Padrão: sempre</span><span class="sxs-lookup"><span data-stu-id="3d54b-166">Default: Always</span></span>

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

### <span data-ttu-id="3d54b-167">-Marca</span><span class="sxs-lookup"><span data-stu-id="3d54b-167">-Tag</span></span>
<span data-ttu-id="3d54b-168">{{Descrição da marca de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="3d54b-168">{{Fill Tag Description}}</span></span>

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

### <span data-ttu-id="3d54b-169">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3d54b-169">-Confirm</span></span>
<span data-ttu-id="3d54b-170">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d54b-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d54b-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d54b-171">-WhatIf</span></span>
<span data-ttu-id="3d54b-172">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3d54b-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d54b-173">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3d54b-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d54b-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d54b-174">CommonParameters</span></span>
<span data-ttu-id="3d54b-175">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d54b-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d54b-176">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d54b-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d54b-177">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3d54b-177">INPUTS</span></span>

### <span data-ttu-id="3d54b-178">System. String</span><span class="sxs-lookup"><span data-stu-id="3d54b-178">System.String</span></span>

### <span data-ttu-id="3d54b-179">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3d54b-179">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3d54b-180">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3d54b-180">OUTPUTS</span></span>

### <span data-ttu-id="3d54b-181">Microsoft. Azure. Commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="3d54b-181">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="3d54b-182">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3d54b-182">NOTES</span></span>

## <span data-ttu-id="3d54b-183">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3d54b-183">RELATED LINKS</span></span>
