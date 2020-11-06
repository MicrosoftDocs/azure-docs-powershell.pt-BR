---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: EC8C915A-A0BC-41DE-9DBF-3617536E3D1A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmContainerServiceConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmContainerServiceConfig.md
ms.openlocfilehash: e88f1d3ce684881d839574fe0b73f36b83e275f9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93611004"
---
# <span data-ttu-id="4349f-101">New-AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="4349f-101">New-AzureRmContainerServiceConfig</span></span>

## <span data-ttu-id="4349f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4349f-102">SYNOPSIS</span></span>
<span data-ttu-id="4349f-103">Cria um objeto de configuração local para um serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="4349f-103">Creates a local configuration object for a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4349f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4349f-104">SYNTAX</span></span>

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

## <span data-ttu-id="4349f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4349f-105">DESCRIPTION</span></span>
<span data-ttu-id="4349f-106">O cmdlet **New-AzureRmContainerServiceConfig** cria um objeto de configuração local para um serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="4349f-106">The **New-AzureRmContainerServiceConfig** cmdlet creates a local configuration object for a container service.</span></span>
<span data-ttu-id="4349f-107">Forneça esse objeto para o cmdlet New-AzureRmContainerService para criar um serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="4349f-107">Provide this object to the New-AzureRmContainerService cmdlet to create a container service.</span></span>

## <span data-ttu-id="4349f-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4349f-108">EXAMPLES</span></span>

### <span data-ttu-id="4349f-109">Exemplo 1: criar uma configuração de serviço de contêiner</span><span class="sxs-lookup"><span data-stu-id="4349f-109">Example 1: Create a container service configuration</span></span>
```
PS C:\> $Container = New-AzureRmContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>" | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="4349f-110">Esse comando cria um contêiner e, em seguida, armazena-o na variável $Container.</span><span class="sxs-lookup"><span data-stu-id="4349f-110">This command creates a container, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="4349f-111">O comando especifica várias configurações para a configuração do serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="4349f-111">The command specifies various settings for the container service configuration.</span></span>
<span data-ttu-id="4349f-112">O comando passa o objeto de configuração para o cmdlet Add-AzureRmContainerServiceAgentPoolProfile usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="4349f-112">The command passes the configuration object to the Add-AzureRmContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4349f-113">Esse cmdlet adiciona um perfil de pool do agente.</span><span class="sxs-lookup"><span data-stu-id="4349f-113">That cmdlet adds an agent pool profile.</span></span>

<span data-ttu-id="4349f-114">Especifique o objeto no $Container para o parâmetro *ContainerService* de **New-AzureRmContainerService**.</span><span class="sxs-lookup"><span data-stu-id="4349f-114">Specify the object in $Container for the *ContainerService* parameter of **New-AzureRmContainerService**.</span></span>

## <span data-ttu-id="4349f-115">OS</span><span class="sxs-lookup"><span data-stu-id="4349f-115">PARAMETERS</span></span>

### <span data-ttu-id="4349f-116">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="4349f-116">-AdminUsername</span></span>
<span data-ttu-id="4349f-117">Especifica o nome da conta de administrador a ser usada para um serviço de contêiner baseado em Linux.</span><span class="sxs-lookup"><span data-stu-id="4349f-117">Specifies the administrator account name to use for a Linux-based container service.</span></span>

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

### <span data-ttu-id="4349f-118">-AgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="4349f-118">-AgentPoolProfile</span></span>
<span data-ttu-id="4349f-119">Especifica uma matriz de objetos de perfil do pool do agente para o serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="4349f-119">Specifies an array of agent pool profile objects for the container service.</span></span>
<span data-ttu-id="4349f-120">Adicione um perfil usando o cmdlet Add-AzureRmContainerServiceAgentPoolProfile.</span><span class="sxs-lookup"><span data-stu-id="4349f-120">Add a profile by using the Add-AzureRmContainerServiceAgentPoolProfile cmdlet.</span></span>

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

### <span data-ttu-id="4349f-121">-CustomProfileOrchestrator</span><span class="sxs-lookup"><span data-stu-id="4349f-121">-CustomProfileOrchestrator</span></span>
<span data-ttu-id="4349f-122">Especifica o organizador de perfil personalizado.</span><span class="sxs-lookup"><span data-stu-id="4349f-122">Specifies the custom profile orchestrator.</span></span>

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

### <span data-ttu-id="4349f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4349f-123">-DefaultProfile</span></span>
<span data-ttu-id="4349f-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4349f-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4349f-125">-Local</span><span class="sxs-lookup"><span data-stu-id="4349f-125">-Location</span></span>
<span data-ttu-id="4349f-126">Especifica o local no qual criar o serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="4349f-126">Specifies the location in which to create the container service.</span></span>

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

### <span data-ttu-id="4349f-127">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="4349f-127">-MasterCount</span></span>
<span data-ttu-id="4349f-128">Especifica o número de máquinas virtuais mestras a serem criadas.</span><span class="sxs-lookup"><span data-stu-id="4349f-128">Specifies the number of master virtual machines to create.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4349f-129">-MasterDnsPrefix</span><span class="sxs-lookup"><span data-stu-id="4349f-129">-MasterDnsPrefix</span></span>
<span data-ttu-id="4349f-130">Especifica o prefixo DNS para a máquina virtual mestre.</span><span class="sxs-lookup"><span data-stu-id="4349f-130">Specifies the DNS prefix for the master virtual machine.</span></span>

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

### <span data-ttu-id="4349f-131">-OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="4349f-131">-OrchestratorType</span></span>
<span data-ttu-id="4349f-132">Especifica o tipo de orquestrador para o serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="4349f-132">Specifies the type of orchestrator for the container service.</span></span>
<span data-ttu-id="4349f-133">Os valores aceitáveis para esse parâmetro são: DCOS e Swarm.</span><span class="sxs-lookup"><span data-stu-id="4349f-133">The acceptable values for this parameter are: DCOS and Swarm.</span></span>

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

### <span data-ttu-id="4349f-134">-ServicePrincipalProfileClientId</span><span class="sxs-lookup"><span data-stu-id="4349f-134">-ServicePrincipalProfileClientId</span></span>
<span data-ttu-id="4349f-135">Especifica a ID de cliente do perfil principal.</span><span class="sxs-lookup"><span data-stu-id="4349f-135">Specifies the principal profile client ID.</span></span>

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

### <span data-ttu-id="4349f-136">-ServicePrincipalProfileSecret</span><span class="sxs-lookup"><span data-stu-id="4349f-136">-ServicePrincipalProfileSecret</span></span>
<span data-ttu-id="4349f-137">Especifica o segredo do perfil principal.</span><span class="sxs-lookup"><span data-stu-id="4349f-137">Specifies the principal profile secret.</span></span>

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

### <span data-ttu-id="4349f-138">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="4349f-138">-SshPublicKey</span></span>
<span data-ttu-id="4349f-139">Especifica a chave pública SSH para um serviço de contêiner baseado em Linux.</span><span class="sxs-lookup"><span data-stu-id="4349f-139">Specifies the SSH public key for a Linux-based container service.</span></span>

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

### <span data-ttu-id="4349f-140">-Marca</span><span class="sxs-lookup"><span data-stu-id="4349f-140">-Tag</span></span>
<span data-ttu-id="4349f-141">Especifica as marcas para o serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="4349f-141">Specifies tags for the container service.</span></span>

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

### <span data-ttu-id="4349f-142">-VmDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="4349f-142">-VmDiagnosticsEnabled</span></span>
<span data-ttu-id="4349f-143">Indica se essa configuração habilita o diagnóstico para a máquina virtual de serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="4349f-143">Indicates whether this configuration enables diagnostics for the container service virtual machine.</span></span>

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

### <span data-ttu-id="4349f-144">-WindowsProfileAdminPassword</span><span class="sxs-lookup"><span data-stu-id="4349f-144">-WindowsProfileAdminPassword</span></span>
<span data-ttu-id="4349f-145">Especifica a senha de administrador para um serviço de contêiner que usa o sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="4349f-145">Specifies the administrator password for a container service that uses the Windows operating system.</span></span>

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

### <span data-ttu-id="4349f-146">-WindowsProfileAdminUsername</span><span class="sxs-lookup"><span data-stu-id="4349f-146">-WindowsProfileAdminUsername</span></span>
<span data-ttu-id="4349f-147">Especifica o nome de usuário administrador para um serviço de contêiner que usa o sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="4349f-147">Specifies the administrator username for a container service that uses the Windows operating system.</span></span>

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

### <span data-ttu-id="4349f-148">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4349f-148">-Confirm</span></span>
<span data-ttu-id="4349f-149">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4349f-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4349f-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4349f-150">-WhatIf</span></span>
<span data-ttu-id="4349f-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4349f-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4349f-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4349f-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4349f-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4349f-153">CommonParameters</span></span>
<span data-ttu-id="4349f-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4349f-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4349f-155">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4349f-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4349f-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4349f-156">INPUTS</span></span>

## <span data-ttu-id="4349f-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4349f-157">OUTPUTS</span></span>

## <span data-ttu-id="4349f-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4349f-158">NOTES</span></span>

## <span data-ttu-id="4349f-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4349f-159">RELATED LINKS</span></span>

[<span data-ttu-id="4349f-160">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="4349f-160">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="4349f-161">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="4349f-161">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)


