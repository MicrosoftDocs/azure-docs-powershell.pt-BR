---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/New-AzureRmContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/New-AzureRmContainerGroup.md
ms.openlocfilehash: 63c54c5f1bb17af82e353b70e757bf91b1208958
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433160"
---
# <span data-ttu-id="21e18-101">New-AzureRmContainerGroup</span><span class="sxs-lookup"><span data-stu-id="21e18-101">New-AzureRmContainerGroup</span></span>

## <span data-ttu-id="21e18-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="21e18-102">SYNOPSIS</span></span>
<span data-ttu-id="21e18-103">Cria um grupo de contêineres.</span><span class="sxs-lookup"><span data-stu-id="21e18-103">Creates a container group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21e18-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="21e18-104">SYNTAX</span></span>

### <span data-ttu-id="21e18-105">CreateContainerGroupBaseParamSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="21e18-105">CreateContainerGroupBaseParamSet (Default)</span></span>
```
New-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> -Image <String> [-Location <String>]
 [-OsType <String>] [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>] [-Port <Int32>]
 [-Command <String>] [-EnvironmentVariable <Hashtable>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21e18-106">CreateContainerGroupWithRegistryParamSet</span><span class="sxs-lookup"><span data-stu-id="21e18-106">CreateContainerGroupWithRegistryParamSet</span></span>
```
New-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> -Image <String> [-Location <String>]
 [-OsType <String>] [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>] [-Port <Int32>]
 [-Command <String>] [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>]
 -RegistryCredential <PSCredential> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21e18-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="21e18-107">DESCRIPTION</span></span>
<span data-ttu-id="21e18-108">Os cmdlets **New-AzureRmContainerGroup** criam um grupo de contêineres.</span><span class="sxs-lookup"><span data-stu-id="21e18-108">The **New-AzureRmContainerGroup** cmdlets creates a container group.</span></span>

## <span data-ttu-id="21e18-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="21e18-109">EXAMPLES</span></span>

### <span data-ttu-id="21e18-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="21e18-110">Example 1</span></span>
```
PS C:\> New-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer -Image nginx -OsType Linux -IpAddressType Public -Port 8000

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
```

<span data-ttu-id="21e18-111">Esses comandos criam um grupo de contêineres usando a imagem Nginx mais recente e solicita um endereço IP público com a porta de abertura 8000.</span><span class="sxs-lookup"><span data-stu-id="21e18-111">This commands creates a container group using latest nginx image and requests a public IP address with opening port 8000.</span></span>

### <span data-ttu-id="21e18-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="21e18-112">Example 2</span></span>
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
```

<span data-ttu-id="21e18-113">Esses comandos criam um grupo de contêineres e executam um script personalizado dentro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="21e18-113">This commands creates a container group and runs a custom script inside the container.</span></span>

### <span data-ttu-id="21e18-114">Exemplo 3: cria um grupo de contêineres usando a imagem no registro do contêiner do Azure</span><span class="sxs-lookup"><span data-stu-id="21e18-114">Example 3: Creates a container group using image in Azure Container Registry</span></span>
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
```

<span data-ttu-id="21e18-115">Esses comandos criam um grupo de contêineres usando uma imagem de Nginx no registro do contêiner do Azure.</span><span class="sxs-lookup"><span data-stu-id="21e18-115">This commands creates a container group using a nginx image in Azure Container Registry.</span></span>

### <span data-ttu-id="21e18-116">Exemplo 4: cria um grupo de contêineres usando a imagem no registro de imagem do contêiner personalizado</span><span class="sxs-lookup"><span data-stu-id="21e18-116">Example 4: Creates a container group using image in custom container image registry</span></span>
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
```

<span data-ttu-id="21e18-117">Esses comandos criam um grupo de contêineres usando uma imagem personalizada de um registro de imagem de contêiner personalizado.</span><span class="sxs-lookup"><span data-stu-id="21e18-117">This commands creates a container group using a custom image from a custom container image registry.</span></span>

## <span data-ttu-id="21e18-118">OS</span><span class="sxs-lookup"><span data-stu-id="21e18-118">PARAMETERS</span></span>

### <span data-ttu-id="21e18-119">-Comando</span><span class="sxs-lookup"><span data-stu-id="21e18-119">-Command</span></span>
<span data-ttu-id="21e18-120">O comando a ser executado no contêiner.</span><span class="sxs-lookup"><span data-stu-id="21e18-120">The command to run in the container.</span></span>

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

### <span data-ttu-id="21e18-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="21e18-121">-Confirm</span></span>
<span data-ttu-id="21e18-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21e18-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21e18-123">-CPU</span><span class="sxs-lookup"><span data-stu-id="21e18-123">-Cpu</span></span>
<span data-ttu-id="21e18-124">Os núcleos de CPU obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="21e18-124">The required CPU cores.</span></span>
<span data-ttu-id="21e18-125">Padrão: 1</span><span class="sxs-lookup"><span data-stu-id="21e18-125">Default: 1</span></span>

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

### <span data-ttu-id="21e18-126">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="21e18-126">-EnvironmentVariable</span></span>
<span data-ttu-id="21e18-127">As variáveis de ambiente do contêiner.</span><span class="sxs-lookup"><span data-stu-id="21e18-127">The container environment variables.</span></span>

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

### <span data-ttu-id="21e18-128">-Imagem</span><span class="sxs-lookup"><span data-stu-id="21e18-128">-Image</span></span>
<span data-ttu-id="21e18-129">A imagem do contêiner.</span><span class="sxs-lookup"><span data-stu-id="21e18-129">The container image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21e18-130">-IpAddresstype</span><span class="sxs-lookup"><span data-stu-id="21e18-130">-IpAddressType</span></span>
<span data-ttu-id="21e18-131">O tipo de endereço IP.</span><span class="sxs-lookup"><span data-stu-id="21e18-131">The IP address type.</span></span>

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

### <span data-ttu-id="21e18-132">-Local</span><span class="sxs-lookup"><span data-stu-id="21e18-132">-Location</span></span>
<span data-ttu-id="21e18-133">O local do grupo de contêineres.</span><span class="sxs-lookup"><span data-stu-id="21e18-133">The container group Location.</span></span>
<span data-ttu-id="21e18-134">Padrão para o local do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="21e18-134">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="21e18-135">-MemoryInGB</span><span class="sxs-lookup"><span data-stu-id="21e18-135">-MemoryInGB</span></span>
<span data-ttu-id="21e18-136">A memória necessária em GB.</span><span class="sxs-lookup"><span data-stu-id="21e18-136">The required memory in GB.</span></span>
<span data-ttu-id="21e18-137">Padrão: 1,5</span><span class="sxs-lookup"><span data-stu-id="21e18-137">Default: 1.5</span></span>

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

### <span data-ttu-id="21e18-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="21e18-138">-Name</span></span>
<span data-ttu-id="21e18-139">O nome do grupo de contêineres.</span><span class="sxs-lookup"><span data-stu-id="21e18-139">The container group name.</span></span>

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

### <span data-ttu-id="21e18-140">-OsType</span><span class="sxs-lookup"><span data-stu-id="21e18-140">-OsType</span></span>
<span data-ttu-id="21e18-141">O tipo de sistema operacional do contêiner.</span><span class="sxs-lookup"><span data-stu-id="21e18-141">The container OS type.</span></span>
<span data-ttu-id="21e18-142">Padrão: Linux</span><span class="sxs-lookup"><span data-stu-id="21e18-142">Default: Linux</span></span>

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

### <span data-ttu-id="21e18-143">-Porta</span><span class="sxs-lookup"><span data-stu-id="21e18-143">-Port</span></span>
<span data-ttu-id="21e18-144">A porta a ser aberta.</span><span class="sxs-lookup"><span data-stu-id="21e18-144">The port to open.</span></span>
<span data-ttu-id="21e18-145">Padrão: 80</span><span class="sxs-lookup"><span data-stu-id="21e18-145">Default: 80</span></span>

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

### <span data-ttu-id="21e18-146">-RegistryCredential</span><span class="sxs-lookup"><span data-stu-id="21e18-146">-RegistryCredential</span></span>
<span data-ttu-id="21e18-147">A credencial personalizada do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="21e18-147">The custom container registry credential.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: CreateContainerGroupWithRegistryParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21e18-148">-RegistryServerDomain</span><span class="sxs-lookup"><span data-stu-id="21e18-148">-RegistryServerDomain</span></span>
<span data-ttu-id="21e18-149">O servidor de logon do contêiner de contêiner personalizado.</span><span class="sxs-lookup"><span data-stu-id="21e18-149">The custom container registry login server.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateContainerGroupWithRegistryParamSet
Aliases: RegistryServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21e18-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21e18-150">-ResourceGroupName</span></span>
<span data-ttu-id="21e18-151">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="21e18-151">The resource group name.</span></span>

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

### <span data-ttu-id="21e18-152">-Marca</span><span class="sxs-lookup"><span data-stu-id="21e18-152">-Tag</span></span>
<span data-ttu-id="21e18-153">{{Descrição da marca de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="21e18-153">{{Fill Tag Description}}</span></span>

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

### <span data-ttu-id="21e18-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21e18-154">-WhatIf</span></span>
<span data-ttu-id="21e18-155">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="21e18-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21e18-156">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="21e18-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21e18-157">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21e18-157">-DefaultProfile</span></span>
<span data-ttu-id="21e18-158">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="21e18-158">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21e18-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21e18-159">CommonParameters</span></span>
<span data-ttu-id="21e18-160">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21e18-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21e18-161">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21e18-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21e18-162">SENSORES</span><span class="sxs-lookup"><span data-stu-id="21e18-162">INPUTS</span></span>

### <span data-ttu-id="21e18-163">System. String</span><span class="sxs-lookup"><span data-stu-id="21e18-163">System.String</span></span>
<span data-ttu-id="21e18-164">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="21e18-164">System.Collections.Hashtable</span></span>

## <span data-ttu-id="21e18-165">EXIBE</span><span class="sxs-lookup"><span data-stu-id="21e18-165">OUTPUTS</span></span>

### <span data-ttu-id="21e18-166">Microsoft. Azure. Commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="21e18-166">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="21e18-167">INFORMA</span><span class="sxs-lookup"><span data-stu-id="21e18-167">NOTES</span></span>

## <span data-ttu-id="21e18-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="21e18-168">RELATED LINKS</span></span>

