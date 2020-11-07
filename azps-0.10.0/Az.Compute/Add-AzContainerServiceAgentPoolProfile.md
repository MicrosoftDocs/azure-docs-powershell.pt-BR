---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: C3C65F3E-1192-4B57-87DB-5D371C8FF68E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azcontainerserviceagentpoolprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzContainerServiceAgentPoolProfile.md
ms.openlocfilehash: c1a3cf88350c02359633d73b074ea1faa910bde9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775221"
---
# <span data-ttu-id="19072-101">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="19072-101">Add-AzContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="19072-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="19072-102">SYNOPSIS</span></span>
<span data-ttu-id="19072-103">Adiciona um perfil de pool de agente de serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="19072-103">Adds a container service agent pool profile.</span></span>

## <span data-ttu-id="19072-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="19072-104">SYNTAX</span></span>

```
Add-AzContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [[-Name] <String>]
 [[-Count] <Int32>] [[-VmSize] <String>] [[-DnsPrefix] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19072-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="19072-105">DESCRIPTION</span></span>
<span data-ttu-id="19072-106">O cmdlet **Add-AzContainerServiceAgentPoolProfile** adiciona um perfil de pool de agente de serviço de contêiner a um objeto de serviço de contêiner local.</span><span class="sxs-lookup"><span data-stu-id="19072-106">The **Add-AzContainerServiceAgentPoolProfile** cmdlet adds a container service agent pool profile to a local container service object.</span></span>

## <span data-ttu-id="19072-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="19072-107">EXAMPLES</span></span>

### <span data-ttu-id="19072-108">Exemplo 1: adicionar um perfil</span><span class="sxs-lookup"><span data-stu-id="19072-108">Example 1: Add a profile</span></span>
```
PS C:\> Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="19072-109">Esse comando adiciona um perfil de pool de agente de serviço de contêiner ao objeto de serviço de contêiner local.</span><span class="sxs-lookup"><span data-stu-id="19072-109">This command adds a container service agent pool profile to the local container service object.</span></span>

## <span data-ttu-id="19072-110">OS</span><span class="sxs-lookup"><span data-stu-id="19072-110">PARAMETERS</span></span>

### <span data-ttu-id="19072-111">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="19072-111">-ContainerService</span></span>
<span data-ttu-id="19072-112">Especifica o objeto de serviço de contêiner para o qual esse cmdlet adiciona um perfil de pool do agente.</span><span class="sxs-lookup"><span data-stu-id="19072-112">Specifies the container service object to which this cmdlet adds an agent pool profile.</span></span>
<span data-ttu-id="19072-113">Para obter um objeto **ContainerService** , use o cmdlet [New-AzContainerServiceConfig](./New-AzContainerServiceConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="19072-113">To obtain a **ContainerService** object, use the [New-AzContainerServiceConfig](./New-AzContainerServiceConfig.md) cmdlet.</span></span>

```yaml
Type: PSContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19072-114">-Contagem</span><span class="sxs-lookup"><span data-stu-id="19072-114">-Count</span></span>
<span data-ttu-id="19072-115">Especifica o número de agentes que hospedam contêineres.</span><span class="sxs-lookup"><span data-stu-id="19072-115">Specifies the number of agents that host containers.</span></span>
<span data-ttu-id="19072-116">Os valores aceitáveis para esse parâmetro são: inteiros de 1 a 100.</span><span class="sxs-lookup"><span data-stu-id="19072-116">The acceptable values for this parameter are: integers from 1 to 100.</span></span>
<span data-ttu-id="19072-117">O valor padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="19072-117">The default value is 1.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19072-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19072-118">-DefaultProfile</span></span>
<span data-ttu-id="19072-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="19072-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19072-120">-DnsPrefix</span><span class="sxs-lookup"><span data-stu-id="19072-120">-DnsPrefix</span></span>
<span data-ttu-id="19072-121">Especifica o prefixo DNS que este cmdlet usa para criar o nome de domínio totalmente qualificado para esse pool de agentes.</span><span class="sxs-lookup"><span data-stu-id="19072-121">Specifies the DNS prefix that this cmdlet uses to create the fully qualified domain name for this agent pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19072-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="19072-122">-Name</span></span>
<span data-ttu-id="19072-123">Especifica o nome do perfil do pool do agente.</span><span class="sxs-lookup"><span data-stu-id="19072-123">Specifies the name of the agent pool profile.</span></span>
<span data-ttu-id="19072-124">Esse valor deve ser exclusivo no contexto da assinatura e do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="19072-124">This value must be unique in the context of the subscription and resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19072-125">-VmSize</span><span class="sxs-lookup"><span data-stu-id="19072-125">-VmSize</span></span>
<span data-ttu-id="19072-126">Especifica o tamanho das máquinas virtuais para os agentes.</span><span class="sxs-lookup"><span data-stu-id="19072-126">Specifies the size of the virtual machines for the agents.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19072-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="19072-127">-Confirm</span></span>
<span data-ttu-id="19072-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19072-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19072-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19072-129">-WhatIf</span></span>
<span data-ttu-id="19072-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="19072-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="19072-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="19072-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19072-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19072-132">CommonParameters</span></span>
<span data-ttu-id="19072-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19072-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19072-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19072-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19072-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="19072-135">INPUTS</span></span>

### <span data-ttu-id="19072-136">ContainerService</span><span class="sxs-lookup"><span data-stu-id="19072-136">ContainerService</span></span>
<span data-ttu-id="19072-137">O parâmetro ' ContainerService ' aceita o valor do tipo ' ContainerService ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="19072-137">Parameter 'ContainerService' accepts value of type 'ContainerService' from the pipeline</span></span>

## <span data-ttu-id="19072-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="19072-138">OUTPUTS</span></span>

### <span data-ttu-id="19072-139">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="19072-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="19072-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="19072-140">NOTES</span></span>

## <span data-ttu-id="19072-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="19072-141">RELATED LINKS</span></span>

[<span data-ttu-id="19072-142">New-AzContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="19072-142">New-AzContainerServiceConfig</span></span>](./New-AzContainerServiceConfig.md)

[<span data-ttu-id="19072-143">Remove-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="19072-143">Remove-AzContainerServiceAgentPoolProfile</span></span>](./Remove-AzContainerServiceAgentPoolProfile.md)