---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: C3C65F3E-1192-4B57-87DB-5D371C8FF68E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmContainerServiceAgentPoolProfile.md
ms.openlocfilehash: 1b3df5b930cd7b30af8fef35735eea56eab7a5da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431724"
---
# <span data-ttu-id="81925-101">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="81925-101">Add-AzureRmContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="81925-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="81925-102">SYNOPSIS</span></span>
<span data-ttu-id="81925-103">Adiciona um perfil de pool de agente de serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="81925-103">Adds a container service agent pool profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81925-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="81925-104">SYNTAX</span></span>

```
Add-AzureRmContainerServiceAgentPoolProfile [-ContainerService] <ContainerService> [[-Name] <String>]
 [[-Count] <Int32>] [[-VmSize] <String>] [[-DnsPrefix] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81925-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="81925-105">DESCRIPTION</span></span>
<span data-ttu-id="81925-106">O cmdlet **Add-AzureRmContainerServiceAgentPoolProfile** adiciona um perfil de pool de agente de serviço de contêiner a um objeto de serviço de contêiner local.</span><span class="sxs-lookup"><span data-stu-id="81925-106">The **Add-AzureRmContainerServiceAgentPoolProfile** cmdlet adds a container service agent pool profile to a local container service object.</span></span>

## <span data-ttu-id="81925-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="81925-107">EXAMPLES</span></span>

### <span data-ttu-id="81925-108">Exemplo 1: adicionar um perfil</span><span class="sxs-lookup"><span data-stu-id="81925-108">Example 1: Add a profile</span></span>
```
PS C:\> Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="81925-109">Esse comando adiciona um perfil de pool de agente de serviço de contêiner ao objeto de serviço de contêiner local.</span><span class="sxs-lookup"><span data-stu-id="81925-109">This command adds a container service agent pool profile to the local container service object.</span></span>

## <span data-ttu-id="81925-110">OS</span><span class="sxs-lookup"><span data-stu-id="81925-110">PARAMETERS</span></span>

### <span data-ttu-id="81925-111">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="81925-111">-ContainerService</span></span>
<span data-ttu-id="81925-112">Especifica o objeto de serviço de contêiner para o qual esse cmdlet adiciona um perfil de pool do agente.</span><span class="sxs-lookup"><span data-stu-id="81925-112">Specifies the container service object to which this cmdlet adds an agent pool profile.</span></span>
<span data-ttu-id="81925-113">Para obter um objeto **ContainerService** , use o cmdlet [New-AzureRmContainerServiceConfig](./New-AzureRmContainerServiceConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="81925-113">To obtain a **ContainerService** object, use the [New-AzureRmContainerServiceConfig](./New-AzureRmContainerServiceConfig.md) cmdlet.</span></span>

```yaml
Type: ContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81925-114">-Contagem</span><span class="sxs-lookup"><span data-stu-id="81925-114">-Count</span></span>
<span data-ttu-id="81925-115">Especifica o número de agentes que hospedam contêineres.</span><span class="sxs-lookup"><span data-stu-id="81925-115">Specifies the number of agents that host containers.</span></span>
<span data-ttu-id="81925-116">Os valores aceitáveis para esse parâmetro são: inteiros de 1 a 100.</span><span class="sxs-lookup"><span data-stu-id="81925-116">The acceptable values for this parameter are: integers from 1 to 100.</span></span>
<span data-ttu-id="81925-117">O valor padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="81925-117">The default value is 1.</span></span>

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

### <span data-ttu-id="81925-118">-DnsPrefix</span><span class="sxs-lookup"><span data-stu-id="81925-118">-DnsPrefix</span></span>
<span data-ttu-id="81925-119">Especifica o prefixo DNS que este cmdlet usa para criar o nome de domínio totalmente qualificado para esse pool de agentes.</span><span class="sxs-lookup"><span data-stu-id="81925-119">Specifies the DNS prefix that this cmdlet uses to create the fully qualified domain name for this agent pool.</span></span>

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

### <span data-ttu-id="81925-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="81925-120">-Name</span></span>
<span data-ttu-id="81925-121">Especifica o nome do perfil do pool do agente.</span><span class="sxs-lookup"><span data-stu-id="81925-121">Specifies the name of the agent pool profile.</span></span>
<span data-ttu-id="81925-122">Esse valor deve ser exclusivo no contexto da assinatura e do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="81925-122">This value must be unique in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="81925-123">-VmSize</span><span class="sxs-lookup"><span data-stu-id="81925-123">-VmSize</span></span>
<span data-ttu-id="81925-124">Especifica o tamanho das máquinas virtuais para os agentes.</span><span class="sxs-lookup"><span data-stu-id="81925-124">Specifies the size of the virtual machines for the agents.</span></span>

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

### <span data-ttu-id="81925-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="81925-125">-Confirm</span></span>
<span data-ttu-id="81925-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81925-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81925-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81925-127">-WhatIf</span></span>
<span data-ttu-id="81925-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="81925-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="81925-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="81925-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81925-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81925-130">CommonParameters</span></span>
<span data-ttu-id="81925-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81925-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81925-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81925-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81925-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="81925-133">INPUTS</span></span>

### <span data-ttu-id="81925-134">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="81925-134">None</span></span>
<span data-ttu-id="81925-135">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="81925-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="81925-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="81925-136">OUTPUTS</span></span>

## <span data-ttu-id="81925-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="81925-137">NOTES</span></span>

## <span data-ttu-id="81925-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="81925-138">RELATED LINKS</span></span>

[<span data-ttu-id="81925-139">New-AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="81925-139">New-AzureRmContainerServiceConfig</span></span>](./New-AzureRmContainerServiceConfig.md)

[<span data-ttu-id="81925-140">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="81925-140">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>](./Remove-AzureRmContainerServiceAgentPoolProfile.md)
