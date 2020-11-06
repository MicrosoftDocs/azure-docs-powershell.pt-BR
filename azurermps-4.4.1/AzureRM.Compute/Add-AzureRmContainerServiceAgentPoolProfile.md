---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: C3C65F3E-1192-4B57-87DB-5D371C8FF68E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmContainerServiceAgentPoolProfile.md
ms.openlocfilehash: a5ce087e8ebf768b63d09a4002c3aaf38ddd9f84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441188"
---
# <span data-ttu-id="5ff40-101">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="5ff40-101">Add-AzureRmContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="5ff40-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5ff40-102">SYNOPSIS</span></span>
<span data-ttu-id="5ff40-103">Adiciona um perfil de pool de agente de serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="5ff40-103">Adds a container service agent pool profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ff40-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5ff40-104">SYNTAX</span></span>

```
Add-AzureRmContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [[-Name] <String>]
 [[-Count] <Int32>] [[-VmSize] <String>] [[-DnsPrefix] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ff40-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5ff40-105">DESCRIPTION</span></span>
<span data-ttu-id="5ff40-106">O cmdlet **Add-AzureRmContainerServiceAgentPoolProfile** adiciona um perfil de pool de agente de serviço de contêiner a um objeto de serviço de contêiner local.</span><span class="sxs-lookup"><span data-stu-id="5ff40-106">The **Add-AzureRmContainerServiceAgentPoolProfile** cmdlet adds a container service agent pool profile to a local container service object.</span></span>

## <span data-ttu-id="5ff40-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5ff40-107">EXAMPLES</span></span>

### <span data-ttu-id="5ff40-108">Exemplo 1: adicionar um perfil</span><span class="sxs-lookup"><span data-stu-id="5ff40-108">Example 1: Add a profile</span></span>
```
PS C:\> Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="5ff40-109">Esse comando adiciona um perfil de pool de agente de serviço de contêiner ao objeto de serviço de contêiner local.</span><span class="sxs-lookup"><span data-stu-id="5ff40-109">This command adds a container service agent pool profile to the local container service object.</span></span>

## <span data-ttu-id="5ff40-110">OS</span><span class="sxs-lookup"><span data-stu-id="5ff40-110">PARAMETERS</span></span>

### <span data-ttu-id="5ff40-111">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="5ff40-111">-ContainerService</span></span>
<span data-ttu-id="5ff40-112">Especifica o objeto de serviço de contêiner para o qual esse cmdlet adiciona um perfil de pool do agente.</span><span class="sxs-lookup"><span data-stu-id="5ff40-112">Specifies the container service object to which this cmdlet adds an agent pool profile.</span></span>
<span data-ttu-id="5ff40-113">Para obter um objeto **ContainerService** , use o cmdlet [New-AzureRmContainerServiceConfig](./New-AzureRmContainerServiceConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="5ff40-113">To obtain a **ContainerService** object, use the [New-AzureRmContainerServiceConfig](./New-AzureRmContainerServiceConfig.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ff40-114">-Contagem</span><span class="sxs-lookup"><span data-stu-id="5ff40-114">-Count</span></span>
<span data-ttu-id="5ff40-115">Especifica o número de agentes que hospedam contêineres.</span><span class="sxs-lookup"><span data-stu-id="5ff40-115">Specifies the number of agents that host containers.</span></span>
<span data-ttu-id="5ff40-116">Os valores aceitáveis para esse parâmetro são: inteiros de 1 a 100.</span><span class="sxs-lookup"><span data-stu-id="5ff40-116">The acceptable values for this parameter are: integers from 1 to 100.</span></span>
<span data-ttu-id="5ff40-117">O valor padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="5ff40-117">The default value is 1.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ff40-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ff40-118">-DefaultProfile</span></span>
<span data-ttu-id="5ff40-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5ff40-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ff40-120">-DnsPrefix</span><span class="sxs-lookup"><span data-stu-id="5ff40-120">-DnsPrefix</span></span>
<span data-ttu-id="5ff40-121">Especifica o prefixo DNS que este cmdlet usa para criar o nome de domínio totalmente qualificado para esse pool de agentes.</span><span class="sxs-lookup"><span data-stu-id="5ff40-121">Specifies the DNS prefix that this cmdlet uses to create the fully qualified domain name for this agent pool.</span></span>

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

### <span data-ttu-id="5ff40-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="5ff40-122">-Name</span></span>
<span data-ttu-id="5ff40-123">Especifica o nome do perfil do pool do agente.</span><span class="sxs-lookup"><span data-stu-id="5ff40-123">Specifies the name of the agent pool profile.</span></span>
<span data-ttu-id="5ff40-124">Esse valor deve ser exclusivo no contexto da assinatura e do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5ff40-124">This value must be unique in the context of the subscription and resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ff40-125">-VmSize</span><span class="sxs-lookup"><span data-stu-id="5ff40-125">-VmSize</span></span>
<span data-ttu-id="5ff40-126">Especifica o tamanho das máquinas virtuais para os agentes.</span><span class="sxs-lookup"><span data-stu-id="5ff40-126">Specifies the size of the virtual machines for the agents.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ff40-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5ff40-127">-Confirm</span></span>
<span data-ttu-id="5ff40-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ff40-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ff40-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ff40-129">-WhatIf</span></span>
<span data-ttu-id="5ff40-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5ff40-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5ff40-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5ff40-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ff40-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ff40-132">CommonParameters</span></span>
<span data-ttu-id="5ff40-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ff40-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ff40-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ff40-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ff40-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5ff40-135">INPUTS</span></span>

## <span data-ttu-id="5ff40-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5ff40-136">OUTPUTS</span></span>

## <span data-ttu-id="5ff40-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5ff40-137">NOTES</span></span>

## <span data-ttu-id="5ff40-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5ff40-138">RELATED LINKS</span></span>

[<span data-ttu-id="5ff40-139">New-AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="5ff40-139">New-AzureRmContainerServiceConfig</span></span>](./New-AzureRmContainerServiceConfig.md)

[<span data-ttu-id="5ff40-140">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="5ff40-140">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>](./Remove-AzureRmContainerServiceAgentPoolProfile.md)
