---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EC8C915A-A0BC-41DE-9DBF-3617536E3D1A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azcontainerserviceconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzContainerServiceConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzContainerServiceConfig.md
ms.openlocfilehash: a2d55c831860f5664f0f8f3dd5312368a9e5da4d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116532"
---
# <span data-ttu-id="f7e4b-101">New-AzContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="f7e4b-101">New-AzContainerServiceConfig</span></span>

## <span data-ttu-id="f7e4b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f7e4b-102">SYNOPSIS</span></span>
<span data-ttu-id="f7e4b-103">Cria um objeto de configuração local para um serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="f7e4b-103">Creates a local configuration object for a container service.</span></span>

## <span data-ttu-id="f7e4b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f7e4b-104">SYNTAX</span></span>

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

## <span data-ttu-id="f7e4b-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="f7e4b-105">DESCRIPTION</span></span>
<span data-ttu-id="f7e4b-106">O cmdlet **New-AzContainerServiceConfig** cria um objeto de configuração local para um serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="f7e4b-106">The **New-AzContainerServiceConfig** cmdlet creates a local configuration object for a container service.</span></span>
<span data-ttu-id="f7e4b-107">Forneça este objeto ao cmdlet New-AzContainerService para criar um serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="f7e4b-107">Provide this object to the New-AzContainerService cmdlet to create a container service.</span></span>

## <span data-ttu-id="f7e4b-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f7e4b-108">EXAMPLES</span></span>

### <span data-ttu-id="f7e4b-109">Exemplo 1: Criar uma configuração de serviço de contêiner</span><span class="sxs-lookup"><span data-stu-id="f7e4b-109">Example 1: Create a container service configuration</span></span>
```
PS C:\> $Container = New-AzContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>"
PS C:\> $Container | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="f7e4b-110">Esse comando cria um contêiner e o armazena na variável $Container dados.</span><span class="sxs-lookup"><span data-stu-id="f7e4b-110">This command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="f7e4b-111">O comando especifica várias configurações para a configuração do serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="f7e4b-111">The command specifies various settings for the container service configuration.</span></span> <span data-ttu-id="f7e4b-112">O comando passa o objeto de configuração para o cmdlet Add-AzContainerServiceAgentPoolProfile usando o operador de pipeline.</span><span class="sxs-lookup"><span data-stu-id="f7e4b-112">The command passes the configuration object to the Add-AzContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span> <span data-ttu-id="f7e4b-113">Esse cmdlet adiciona um perfil de pool de agente.</span><span class="sxs-lookup"><span data-stu-id="f7e4b-113">That cmdlet adds an agent pool profile.</span></span>
<span data-ttu-id="f7e4b-114">Especifique o objeto no $Container para o parâmetro *ContainerService* do **New-AzContainerService.**</span><span class="sxs-lookup"><span data-stu-id="f7e4b-114">Specify the object in $Container for the *ContainerService* parameter of **New-AzContainerService**.</span></span>

## <span data-ttu-id="f7e4b-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f7e4b-115">PARAMETERS</span></span>

### <span data-ttu-id="f7e4b-116">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="f7e4b-116">-AdminUsername</span></span>
<span data-ttu-id="f7e4b-117">Especifica o nome da conta de administrador a ser usada para um serviço de contêiner baseado no Linux.</span><span class="sxs-lookup"><span data-stu-id="f7e4b-117">Specifies the administrator account name to use for a Linux-based container service.</span></span>

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

### <span data-ttu-id="f7e4b-118">-AgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="f7e4b-118">-AgentPoolProfile</span></span>
<span data-ttu-id="f7e4b-119">Especifica uma matriz de objetos de perfil de pool de agente para o serviço de contêineres.</span><span class="sxs-lookup"><span data-stu-id="f7e4b-119">Specifies an array of agent pool profile objects for the container service.</span></span>
<span data-ttu-id="f7e4b-120">Adicione um perfil usando o Add-AzContainerServiceAgentPoolProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7e4b-120">Add a profile by using the Add-AzContainerServiceAgentPoolProfile cmdlet.</span></span>

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

### <span data-ttu-id="f7e4b-121">-CustomProfileOfileOfiletrator</span><span class="sxs-lookup"><span data-stu-id="f7e4b-121">-CustomProfileOrchestrator</span></span>
<span data-ttu-id="f7e4b-122">Especifica o orador de perfil personalizado.</span><span class="sxs-lookup"><span data-stu-id="f7e4b-122">Specifies the custom profile orchestrator.</span></span>

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

### <span data-ttu-id="f7e4b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7e4b-123">-DefaultProfile</span></span>
<span data-ttu-id="f7e4b-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="f7e4b-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7e4b-125">-Local</span><span class="sxs-lookup"><span data-stu-id="f7e4b-125">-Location</span></span>
<span data-ttu-id="f7e4b-126">Especifica o local no qual criar o serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="f7e4b-126">Specifies the location in which to create the container service.</span></span>

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

### <span data-ttu-id="f7e4b-127">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="f7e4b-127">-MasterCount</span></span>
<span data-ttu-id="f7e4b-128">Especifica o número de máquinas virtuais mestras a ser criado.</span><span class="sxs-lookup"><span data-stu-id="f7e4b-128">Specifies the number of master virtual machines to create.</span></span>

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

### <span data-ttu-id="f7e4b-129">-MasterDnsPrefix</span><span class="sxs-lookup"><span data-stu-id="f7e4b-129">-MasterDnsPrefix</span></span>
<span data-ttu-id="f7e4b-130">Especifica o prefixo DNS para a máquina virtual mestra.</span><span class="sxs-lookup"><span data-stu-id="f7e4b-130">Specifies the DNS prefix for the master virtual machine.</span></span>

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

### <span data-ttu-id="f7e4b-131">-OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="f7e4b-131">-OrchestratorType</span></span>
<span data-ttu-id="f7e4b-132">Especifica o tipo de ortador para o serviço de contêineres.</span><span class="sxs-lookup"><span data-stu-id="f7e4b-132">Specifies the type of orchestrator for the container service.</span></span>
<span data-ttu-id="f7e4b-133">Os valores aceitáveis para este parâmetro são: DCOS e Grupo.</span><span class="sxs-lookup"><span data-stu-id="f7e4b-133">The acceptable values for this parameter are: DCOS and Swarm.</span></span>

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

### <span data-ttu-id="f7e4b-134">-ServicePrincipalProfileClientId</span><span class="sxs-lookup"><span data-stu-id="f7e4b-134">-ServicePrincipalProfileClientId</span></span>
<span data-ttu-id="f7e4b-135">Especifica a ID do cliente de perfil principal.</span><span class="sxs-lookup"><span data-stu-id="f7e4b-135">Specifies the principal profile client ID.</span></span>

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

### <span data-ttu-id="f7e4b-136">-ServicePrincipalProfileSecduto</span><span class="sxs-lookup"><span data-stu-id="f7e4b-136">-ServicePrincipalProfileSecret</span></span>
<span data-ttu-id="f7e4b-137">Especifica o segredo do perfil principal.</span><span class="sxs-lookup"><span data-stu-id="f7e4b-137">Specifies the principal profile secret.</span></span>

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

### <span data-ttu-id="f7e4b-138">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="f7e4b-138">-SshPublicKey</span></span>
<span data-ttu-id="f7e4b-139">Especifica a chave pública SSH para um serviço de contêiner baseado no Linux.</span><span class="sxs-lookup"><span data-stu-id="f7e4b-139">Specifies the SSH public key for a Linux-based container service.</span></span>

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

### <span data-ttu-id="f7e4b-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="f7e4b-140">-Tag</span></span>
<span data-ttu-id="f7e4b-141">Pares de valor-chave na forma de uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="f7e4b-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f7e4b-142">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="f7e4b-142">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f7e4b-143">-VmDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="f7e4b-143">-VmDiagnosticsEnabled</span></span>
<span data-ttu-id="f7e4b-144">Indica se essa configuração habilita o diagnóstico para a máquina virtual de serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="f7e4b-144">Indicates whether this configuration enables diagnostics for the container service virtual machine.</span></span>

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

### <span data-ttu-id="f7e4b-145">-WindowsProfileAdminPassword</span><span class="sxs-lookup"><span data-stu-id="f7e4b-145">-WindowsProfileAdminPassword</span></span>
<span data-ttu-id="f7e4b-146">Especifica a senha de administrador de um serviço de contêiner que usa o sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="f7e4b-146">Specifies the administrator password for a container service that uses the Windows operating system.</span></span>

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

### <span data-ttu-id="f7e4b-147">-WindowsProfileAdminUsername</span><span class="sxs-lookup"><span data-stu-id="f7e4b-147">-WindowsProfileAdminUsername</span></span>
<span data-ttu-id="f7e4b-148">Especifica o nome de usuário do administrador para um serviço de contêiner que usa o sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="f7e4b-148">Specifies the administrator username for a container service that uses the Windows operating system.</span></span>

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

### <span data-ttu-id="f7e4b-149">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f7e4b-149">-Confirm</span></span>
<span data-ttu-id="f7e4b-150">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7e4b-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7e4b-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7e4b-151">-WhatIf</span></span>
<span data-ttu-id="f7e4b-152">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="f7e4b-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f7e4b-153">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f7e4b-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7e4b-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7e4b-154">CommonParameters</span></span>
<span data-ttu-id="f7e4b-155">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7e4b-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7e4b-156">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f7e4b-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7e4b-157">Entradas</span><span class="sxs-lookup"><span data-stu-id="f7e4b-157">INPUTS</span></span>

### <span data-ttu-id="f7e4b-158">System.String</span><span class="sxs-lookup"><span data-stu-id="f7e4b-158">System.String</span></span>

### <span data-ttu-id="f7e4b-159">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f7e4b-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f7e4b-160">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.ContainerServiceOkeytratorTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="f7e4b-160">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ContainerServiceOrchestratorTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="f7e4b-161">System.Int32</span><span class="sxs-lookup"><span data-stu-id="f7e4b-161">System.Int32</span></span>

### <span data-ttu-id="f7e4b-162">Microsoft.Azure.Management.Compute.Models.ContainerServiceAgentPoolProfile[]</span><span class="sxs-lookup"><span data-stu-id="f7e4b-162">Microsoft.Azure.Management.Compute.Models.ContainerServiceAgentPoolProfile[]</span></span>

### <span data-ttu-id="f7e4b-163">System.String[]</span><span class="sxs-lookup"><span data-stu-id="f7e4b-163">System.String[]</span></span>

### <span data-ttu-id="f7e4b-164">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f7e4b-164">System.Boolean</span></span>

## <span data-ttu-id="f7e4b-165">Saídas</span><span class="sxs-lookup"><span data-stu-id="f7e4b-165">OUTPUTS</span></span>

### <span data-ttu-id="f7e4b-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="f7e4b-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="f7e4b-167">Notas</span><span class="sxs-lookup"><span data-stu-id="f7e4b-167">NOTES</span></span>

## <span data-ttu-id="f7e4b-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f7e4b-168">RELATED LINKS</span></span>

[<span data-ttu-id="f7e4b-169">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="f7e4b-169">Add-AzContainerServiceAgentPoolProfile</span></span>](./Add-AzContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="f7e4b-170">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="f7e4b-170">New-AzContainerService</span></span>](./New-AzContainerService.md)
