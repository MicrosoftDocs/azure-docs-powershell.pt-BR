---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: EC8C915A-A0BC-41DE-9DBF-3617536E3D1A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermcontainerserviceconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmContainerServiceConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmContainerServiceConfig.md
ms.openlocfilehash: 51ebdbffcb88c1d43716170b236332741d05466f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432047"
---
# <span data-ttu-id="9cbe2-101">New-AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="9cbe2-101">New-AzureRmContainerServiceConfig</span></span>

## <span data-ttu-id="9cbe2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9cbe2-102">SYNOPSIS</span></span>
<span data-ttu-id="9cbe2-103">Cria um objeto de configuração local para um serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-103">Creates a local configuration object for a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9cbe2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9cbe2-104">SYNTAX</span></span>

```
New-AzureRmContainerServiceConfig [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-OrchestratorType] <ContainerServiceOrchestratorTypes>] [[-MasterCount] <Int32>]
 [[-MasterDnsPrefix] <String>] [[-AgentPoolProfile] <ContainerServiceAgentPoolProfile[]>]
 [[-WindowsProfileAdminUsername] <String>] [[-WindowsProfileAdminPassword] <String>]
 [[-AdminUsername] <String>] [[-SshPublicKey] <String[]>] [[-VmDiagnosticsEnabled] <Boolean>]
 [-CustomProfileOrchestrator <String>] [-ServicePrincipalProfileClientId <String>]
 [-ServicePrincipalProfileSecret <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9cbe2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9cbe2-105">DESCRIPTION</span></span>
<span data-ttu-id="9cbe2-106">O cmdlet **New-AzureRmContainerServiceConfig** cria um objeto de configuração local para um serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-106">The **New-AzureRmContainerServiceConfig** cmdlet creates a local configuration object for a container service.</span></span>
<span data-ttu-id="9cbe2-107">Forneça esse objeto para o cmdlet New-AzureRmContainerService para criar um serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-107">Provide this object to the New-AzureRmContainerService cmdlet to create a container service.</span></span>

## <span data-ttu-id="9cbe2-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9cbe2-108">EXAMPLES</span></span>

### <span data-ttu-id="9cbe2-109">Exemplo 1: criar uma configuração de serviço de contêiner</span><span class="sxs-lookup"><span data-stu-id="9cbe2-109">Example 1: Create a container service configuration</span></span>
```
PS C:\> $Container = New-AzureRmContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>"
PS C:\> $Container | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="9cbe2-110">Esse comando cria um contêiner e, em seguida, armazena-o na variável $Container.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-110">This command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="9cbe2-111">O comando especifica várias configurações para a configuração do serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-111">The command specifies various settings for the container service configuration.</span></span> <span data-ttu-id="9cbe2-112">O comando passa o objeto de configuração para o cmdlet Add-AzureRmContainerServiceAgentPoolProfile usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-112">The command passes the configuration object to the Add-AzureRmContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span> <span data-ttu-id="9cbe2-113">Esse cmdlet adiciona um perfil de pool do agente.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-113">That cmdlet adds an agent pool profile.</span></span>
<span data-ttu-id="9cbe2-114">Especifique o objeto no $Container para o parâmetro *ContainerService* de **New-AzureRmContainerService**.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-114">Specify the object in $Container for the *ContainerService* parameter of **New-AzureRmContainerService**.</span></span>

## <span data-ttu-id="9cbe2-115">OS</span><span class="sxs-lookup"><span data-stu-id="9cbe2-115">PARAMETERS</span></span>

### <span data-ttu-id="9cbe2-116">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="9cbe2-116">-AdminUsername</span></span>
<span data-ttu-id="9cbe2-117">Especifica o nome da conta de administrador a ser usada para um serviço de contêiner baseado em Linux.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-117">Specifies the administrator account name to use for a Linux-based container service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cbe2-118">-AgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="9cbe2-118">-AgentPoolProfile</span></span>
<span data-ttu-id="9cbe2-119">Especifica uma matriz de objetos de perfil do pool do agente para o serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-119">Specifies an array of agent pool profile objects for the container service.</span></span>
<span data-ttu-id="9cbe2-120">Adicione um perfil usando o cmdlet Add-AzureRmContainerServiceAgentPoolProfile.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-120">Add a profile by using the Add-AzureRmContainerServiceAgentPoolProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ContainerServiceAgentPoolProfile[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cbe2-121">-CustomProfileOrchestrator</span><span class="sxs-lookup"><span data-stu-id="9cbe2-121">-CustomProfileOrchestrator</span></span>
<span data-ttu-id="9cbe2-122">Especifica o organizador de perfil personalizado.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-122">Specifies the custom profile orchestrator.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cbe2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cbe2-123">-DefaultProfile</span></span>
<span data-ttu-id="9cbe2-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9cbe2-125">-Local</span><span class="sxs-lookup"><span data-stu-id="9cbe2-125">-Location</span></span>
<span data-ttu-id="9cbe2-126">Especifica o local no qual criar o serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-126">Specifies the location in which to create the container service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cbe2-127">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="9cbe2-127">-MasterCount</span></span>
<span data-ttu-id="9cbe2-128">Especifica o número de máquinas virtuais mestras a serem criadas.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-128">Specifies the number of master virtual machines to create.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cbe2-129">-MasterDnsPrefix</span><span class="sxs-lookup"><span data-stu-id="9cbe2-129">-MasterDnsPrefix</span></span>
<span data-ttu-id="9cbe2-130">Especifica o prefixo DNS para a máquina virtual mestre.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-130">Specifies the DNS prefix for the master virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cbe2-131">-OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="9cbe2-131">-OrchestratorType</span></span>
<span data-ttu-id="9cbe2-132">Especifica o tipo de orquestrador para o serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-132">Specifies the type of orchestrator for the container service.</span></span>
<span data-ttu-id="9cbe2-133">Os valores aceitáveis para esse parâmetro são: DCOS e Swarm.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-133">The acceptable values for this parameter are: DCOS and Swarm.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ContainerServiceOrchestratorTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Swarm, DCOS, Custom, Kubernetes

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cbe2-134">-ServicePrincipalProfileClientId</span><span class="sxs-lookup"><span data-stu-id="9cbe2-134">-ServicePrincipalProfileClientId</span></span>
<span data-ttu-id="9cbe2-135">Especifica a ID de cliente do perfil principal.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-135">Specifies the principal profile client ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cbe2-136">-ServicePrincipalProfileSecret</span><span class="sxs-lookup"><span data-stu-id="9cbe2-136">-ServicePrincipalProfileSecret</span></span>
<span data-ttu-id="9cbe2-137">Especifica o segredo do perfil principal.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-137">Specifies the principal profile secret.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cbe2-138">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="9cbe2-138">-SshPublicKey</span></span>
<span data-ttu-id="9cbe2-139">Especifica a chave pública SSH para um serviço de contêiner baseado em Linux.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-139">Specifies the SSH public key for a Linux-based container service.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cbe2-140">-Marca</span><span class="sxs-lookup"><span data-stu-id="9cbe2-140">-Tag</span></span>
<span data-ttu-id="9cbe2-141">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9cbe2-142">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="9cbe2-142">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cbe2-143">-VmDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="9cbe2-143">-VmDiagnosticsEnabled</span></span>
<span data-ttu-id="9cbe2-144">Indica se essa configuração habilita o diagnóstico para a máquina virtual de serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-144">Indicates whether this configuration enables diagnostics for the container service virtual machine.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cbe2-145">-WindowsProfileAdminPassword</span><span class="sxs-lookup"><span data-stu-id="9cbe2-145">-WindowsProfileAdminPassword</span></span>
<span data-ttu-id="9cbe2-146">Especifica a senha de administrador para um serviço de contêiner que usa o sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-146">Specifies the administrator password for a container service that uses the Windows operating system.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cbe2-147">-WindowsProfileAdminUsername</span><span class="sxs-lookup"><span data-stu-id="9cbe2-147">-WindowsProfileAdminUsername</span></span>
<span data-ttu-id="9cbe2-148">Especifica o nome de usuário administrador para um serviço de contêiner que usa o sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-148">Specifies the administrator username for a container service that uses the Windows operating system.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cbe2-149">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9cbe2-149">-Confirm</span></span>
<span data-ttu-id="9cbe2-150">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cbe2-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cbe2-151">-WhatIf</span></span>
<span data-ttu-id="9cbe2-152">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9cbe2-153">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cbe2-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cbe2-154">CommonParameters</span></span>
<span data-ttu-id="9cbe2-155">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cbe2-156">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cbe2-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cbe2-157">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9cbe2-157">INPUTS</span></span>

### <span data-ttu-id="9cbe2-158">System. String</span><span class="sxs-lookup"><span data-stu-id="9cbe2-158">System.String</span></span>

### <span data-ttu-id="9cbe2-159">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9cbe2-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="9cbe2-160">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. Models. ContainerServiceOrchestratorTypes, Microsoft. Azure. Management. Compute, Version = 21.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="9cbe2-160">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ContainerServiceOrchestratorTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="9cbe2-161">System. Int32</span><span class="sxs-lookup"><span data-stu-id="9cbe2-161">System.Int32</span></span>

### <span data-ttu-id="9cbe2-162">Microsoft. Azure. Management. COMPUTE. Models. ContainerServiceAgentPoolProfile []</span><span class="sxs-lookup"><span data-stu-id="9cbe2-162">Microsoft.Azure.Management.Compute.Models.ContainerServiceAgentPoolProfile[]</span></span>

### <span data-ttu-id="9cbe2-163">System. String []</span><span class="sxs-lookup"><span data-stu-id="9cbe2-163">System.String[]</span></span>

### <span data-ttu-id="9cbe2-164">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9cbe2-164">System.Boolean</span></span>

## <span data-ttu-id="9cbe2-165">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9cbe2-165">OUTPUTS</span></span>

### <span data-ttu-id="9cbe2-166">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="9cbe2-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="9cbe2-167">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9cbe2-167">NOTES</span></span>

## <span data-ttu-id="9cbe2-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9cbe2-168">RELATED LINKS</span></span>

[<span data-ttu-id="9cbe2-169">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="9cbe2-169">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="9cbe2-170">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="9cbe2-170">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)