---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EC8C915A-A0BC-41DE-9DBF-3617536E3D1A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azcontainerserviceconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzContainerServiceConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzContainerServiceConfig.md
ms.openlocfilehash: a2d55c831860f5664f0f8f3dd5312368a9e5da4d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434323"
---
# <span data-ttu-id="2a44e-101">New-AzContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="2a44e-101">New-AzContainerServiceConfig</span></span>

## <span data-ttu-id="2a44e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2a44e-102">SYNOPSIS</span></span>
<span data-ttu-id="2a44e-103">Cria um objeto de configuração local para um serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="2a44e-103">Creates a local configuration object for a container service.</span></span>

## <span data-ttu-id="2a44e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2a44e-104">SYNTAX</span></span>

```
New-AzContainerServiceConfig [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-OrchestratorType] <ContainerServiceOrchestratorTypes>] [[-MasterCount] <Int32>]
 [[-MasterDnsPrefix] <String>] [[-AgentPoolProfile] <ContainerServiceAgentPoolProfile[]>]
 [[-WindowsProfileAdminUsername] <String>] [[-WindowsProfileAdminPassword] <String>]
 [[-AdminUsername] <String>] [[-SshPublicKey] <String[]>] [[-VmDiagnosticsEnabled] <Boolean>]
 [-CustomProfileOrchestrator <String>] [-ServicePrincipalProfileClientId <String>]
 [-ServicePrincipalProfileSecret <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2a44e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2a44e-105">DESCRIPTION</span></span>
<span data-ttu-id="2a44e-106">O cmdlet **New-AzContainerServiceConfig** cria um objeto de configuração local para um serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="2a44e-106">The **New-AzContainerServiceConfig** cmdlet creates a local configuration object for a container service.</span></span>
<span data-ttu-id="2a44e-107">Forneça esse objeto para o cmdlet New-AzContainerService para criar um serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="2a44e-107">Provide this object to the New-AzContainerService cmdlet to create a container service.</span></span>

## <span data-ttu-id="2a44e-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2a44e-108">EXAMPLES</span></span>

### <span data-ttu-id="2a44e-109">Exemplo 1: criar uma configuração de serviço de contêiner</span><span class="sxs-lookup"><span data-stu-id="2a44e-109">Example 1: Create a container service configuration</span></span>
```
PS C:\> $Container = New-AzContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>"
PS C:\> $Container | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="2a44e-110">Esse comando cria um contêiner e, em seguida, armazena-o na variável $Container.</span><span class="sxs-lookup"><span data-stu-id="2a44e-110">This command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="2a44e-111">O comando especifica várias configurações para a configuração do serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="2a44e-111">The command specifies various settings for the container service configuration.</span></span> <span data-ttu-id="2a44e-112">O comando passa o objeto de configuração para o cmdlet Add-AzContainerServiceAgentPoolProfile usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="2a44e-112">The command passes the configuration object to the Add-AzContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span> <span data-ttu-id="2a44e-113">Esse cmdlet adiciona um perfil de pool do agente.</span><span class="sxs-lookup"><span data-stu-id="2a44e-113">That cmdlet adds an agent pool profile.</span></span>
<span data-ttu-id="2a44e-114">Especifique o objeto no $Container para o parâmetro *ContainerService* de **New-AzContainerService**.</span><span class="sxs-lookup"><span data-stu-id="2a44e-114">Specify the object in $Container for the *ContainerService* parameter of **New-AzContainerService**.</span></span>

## <span data-ttu-id="2a44e-115">OS</span><span class="sxs-lookup"><span data-stu-id="2a44e-115">PARAMETERS</span></span>

### <span data-ttu-id="2a44e-116">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="2a44e-116">-AdminUsername</span></span>
<span data-ttu-id="2a44e-117">Especifica o nome da conta de administrador a ser usada para um serviço de contêiner baseado em Linux.</span><span class="sxs-lookup"><span data-stu-id="2a44e-117">Specifies the administrator account name to use for a Linux-based container service.</span></span>

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

### <span data-ttu-id="2a44e-118">-AgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="2a44e-118">-AgentPoolProfile</span></span>
<span data-ttu-id="2a44e-119">Especifica uma matriz de objetos de perfil do pool do agente para o serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="2a44e-119">Specifies an array of agent pool profile objects for the container service.</span></span>
<span data-ttu-id="2a44e-120">Adicione um perfil usando o cmdlet Add-AzContainerServiceAgentPoolProfile.</span><span class="sxs-lookup"><span data-stu-id="2a44e-120">Add a profile by using the Add-AzContainerServiceAgentPoolProfile cmdlet.</span></span>

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

### <span data-ttu-id="2a44e-121">-CustomProfileOrchestrator</span><span class="sxs-lookup"><span data-stu-id="2a44e-121">-CustomProfileOrchestrator</span></span>
<span data-ttu-id="2a44e-122">Especifica o organizador de perfil personalizado.</span><span class="sxs-lookup"><span data-stu-id="2a44e-122">Specifies the custom profile orchestrator.</span></span>

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

### <span data-ttu-id="2a44e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a44e-123">-DefaultProfile</span></span>
<span data-ttu-id="2a44e-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2a44e-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a44e-125">-Local</span><span class="sxs-lookup"><span data-stu-id="2a44e-125">-Location</span></span>
<span data-ttu-id="2a44e-126">Especifica o local no qual criar o serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="2a44e-126">Specifies the location in which to create the container service.</span></span>

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

### <span data-ttu-id="2a44e-127">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="2a44e-127">-MasterCount</span></span>
<span data-ttu-id="2a44e-128">Especifica o número de máquinas virtuais mestras a serem criadas.</span><span class="sxs-lookup"><span data-stu-id="2a44e-128">Specifies the number of master virtual machines to create.</span></span>

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

### <span data-ttu-id="2a44e-129">-MasterDnsPrefix</span><span class="sxs-lookup"><span data-stu-id="2a44e-129">-MasterDnsPrefix</span></span>
<span data-ttu-id="2a44e-130">Especifica o prefixo DNS para a máquina virtual mestre.</span><span class="sxs-lookup"><span data-stu-id="2a44e-130">Specifies the DNS prefix for the master virtual machine.</span></span>

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

### <span data-ttu-id="2a44e-131">-OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="2a44e-131">-OrchestratorType</span></span>
<span data-ttu-id="2a44e-132">Especifica o tipo de orquestrador para o serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="2a44e-132">Specifies the type of orchestrator for the container service.</span></span>
<span data-ttu-id="2a44e-133">Os valores aceitáveis para esse parâmetro são: DCOS e Swarm.</span><span class="sxs-lookup"><span data-stu-id="2a44e-133">The acceptable values for this parameter are: DCOS and Swarm.</span></span>

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

### <span data-ttu-id="2a44e-134">-ServicePrincipalProfileClientId</span><span class="sxs-lookup"><span data-stu-id="2a44e-134">-ServicePrincipalProfileClientId</span></span>
<span data-ttu-id="2a44e-135">Especifica a ID de cliente do perfil principal.</span><span class="sxs-lookup"><span data-stu-id="2a44e-135">Specifies the principal profile client ID.</span></span>

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

### <span data-ttu-id="2a44e-136">-ServicePrincipalProfileSecret</span><span class="sxs-lookup"><span data-stu-id="2a44e-136">-ServicePrincipalProfileSecret</span></span>
<span data-ttu-id="2a44e-137">Especifica o segredo do perfil principal.</span><span class="sxs-lookup"><span data-stu-id="2a44e-137">Specifies the principal profile secret.</span></span>

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

### <span data-ttu-id="2a44e-138">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="2a44e-138">-SshPublicKey</span></span>
<span data-ttu-id="2a44e-139">Especifica a chave pública SSH para um serviço de contêiner baseado em Linux.</span><span class="sxs-lookup"><span data-stu-id="2a44e-139">Specifies the SSH public key for a Linux-based container service.</span></span>

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

### <span data-ttu-id="2a44e-140">-Marca</span><span class="sxs-lookup"><span data-stu-id="2a44e-140">-Tag</span></span>
<span data-ttu-id="2a44e-141">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="2a44e-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2a44e-142">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="2a44e-142">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2a44e-143">-VmDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="2a44e-143">-VmDiagnosticsEnabled</span></span>
<span data-ttu-id="2a44e-144">Indica se essa configuração habilita o diagnóstico para a máquina virtual de serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="2a44e-144">Indicates whether this configuration enables diagnostics for the container service virtual machine.</span></span>

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

### <span data-ttu-id="2a44e-145">-WindowsProfileAdminPassword</span><span class="sxs-lookup"><span data-stu-id="2a44e-145">-WindowsProfileAdminPassword</span></span>
<span data-ttu-id="2a44e-146">Especifica a senha de administrador para um serviço de contêiner que usa o sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="2a44e-146">Specifies the administrator password for a container service that uses the Windows operating system.</span></span>

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

### <span data-ttu-id="2a44e-147">-WindowsProfileAdminUsername</span><span class="sxs-lookup"><span data-stu-id="2a44e-147">-WindowsProfileAdminUsername</span></span>
<span data-ttu-id="2a44e-148">Especifica o nome de usuário administrador para um serviço de contêiner que usa o sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="2a44e-148">Specifies the administrator username for a container service that uses the Windows operating system.</span></span>

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

### <span data-ttu-id="2a44e-149">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2a44e-149">-Confirm</span></span>
<span data-ttu-id="2a44e-150">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a44e-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a44e-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a44e-151">-WhatIf</span></span>
<span data-ttu-id="2a44e-152">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2a44e-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2a44e-153">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2a44e-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a44e-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a44e-154">CommonParameters</span></span>
<span data-ttu-id="2a44e-155">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a44e-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a44e-156">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a44e-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a44e-157">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2a44e-157">INPUTS</span></span>

### <span data-ttu-id="2a44e-158">System. String</span><span class="sxs-lookup"><span data-stu-id="2a44e-158">System.String</span></span>

### <span data-ttu-id="2a44e-159">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2a44e-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="2a44e-160">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. Models. ContainerServiceOrchestratorTypes, Microsoft. Azure. Management. Compute, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="2a44e-160">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ContainerServiceOrchestratorTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="2a44e-161">System. Int32</span><span class="sxs-lookup"><span data-stu-id="2a44e-161">System.Int32</span></span>

### <span data-ttu-id="2a44e-162">Microsoft. Azure. Management. COMPUTE. Models. ContainerServiceAgentPoolProfile []</span><span class="sxs-lookup"><span data-stu-id="2a44e-162">Microsoft.Azure.Management.Compute.Models.ContainerServiceAgentPoolProfile[]</span></span>

### <span data-ttu-id="2a44e-163">System. String []</span><span class="sxs-lookup"><span data-stu-id="2a44e-163">System.String[]</span></span>

### <span data-ttu-id="2a44e-164">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2a44e-164">System.Boolean</span></span>

## <span data-ttu-id="2a44e-165">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2a44e-165">OUTPUTS</span></span>

### <span data-ttu-id="2a44e-166">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="2a44e-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="2a44e-167">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2a44e-167">NOTES</span></span>

## <span data-ttu-id="2a44e-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2a44e-168">RELATED LINKS</span></span>

[<span data-ttu-id="2a44e-169">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="2a44e-169">Add-AzContainerServiceAgentPoolProfile</span></span>](./Add-AzContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="2a44e-170">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="2a44e-170">New-AzContainerService</span></span>](./New-AzContainerService.md)
