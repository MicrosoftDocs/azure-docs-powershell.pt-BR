---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: ED37B17D-C513-422A-89EA-A6AF1C9A5FEE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermcontainerserviceagentpoolprofile
schema: 2.0.0
ms.openlocfilehash: 2bbc7d9e1ac125134931be483d3a693252ce12d0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786149"
---
# <span data-ttu-id="f39c6-101">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="f39c6-101">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="f39c6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f39c6-102">SYNOPSIS</span></span>
<span data-ttu-id="f39c6-103">Remove um perfil de pool de agente de um serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="f39c6-103">Removes an agent pool profile from a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f39c6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f39c6-104">SYNTAX</span></span>

```
Remove-AzureRmContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f39c6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f39c6-105">DESCRIPTION</span></span>
<span data-ttu-id="f39c6-106">O cmdlet **Remove-AzureRmContainerServiceAgentPoolProfile** remove um perfil de pool de agente de um serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="f39c6-106">The **Remove-AzureRmContainerServiceAgentPoolProfile** cmdlet removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="f39c6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f39c6-107">EXAMPLES</span></span>

### <span data-ttu-id="f39c6-108">Exemplo 1: remover um perfil de um serviço de contêiner</span><span class="sxs-lookup"><span data-stu-id="f39c6-108">Example 1: Remove a profile from a container service</span></span>
```
PS C:\> $Container = Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" 
PS C:\> Remove-AzureRmContainerServiceAgentPoolProfile -ContainerService $Container -Name "AgentPool01"
```

<span data-ttu-id="f39c6-109">O primeiro comando obtém um serviço de contêiner chamado CSResourceGroup17 usando o cmdlet Get-AzureRmContainerService.</span><span class="sxs-lookup"><span data-stu-id="f39c6-109">The first command gets a container service named CSResourceGroup17 by using the Get-AzureRmContainerService cmdlet.</span></span>
<span data-ttu-id="f39c6-110">O comando armazena o serviço na variável $Container.</span><span class="sxs-lookup"><span data-stu-id="f39c6-110">The command stores the service in the $Container variable.</span></span>

<span data-ttu-id="f39c6-111">O segundo comando Remove o perfil chamado AgentPool01 do serviço de contêiner em $Container.</span><span class="sxs-lookup"><span data-stu-id="f39c6-111">The second command removes the profile named AgentPool01 from the container service in $Container.</span></span>

## <span data-ttu-id="f39c6-112">OS</span><span class="sxs-lookup"><span data-stu-id="f39c6-112">PARAMETERS</span></span>

### <span data-ttu-id="f39c6-113">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="f39c6-113">-ContainerService</span></span>
<span data-ttu-id="f39c6-114">Especifica o objeto de serviço de contêiner do qual esse cmdlet Remove um perfil de pool do agente.</span><span class="sxs-lookup"><span data-stu-id="f39c6-114">Specifies the container service object from which this cmdlet removes an agent pool profile.</span></span>

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

### <span data-ttu-id="f39c6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f39c6-115">-DefaultProfile</span></span>
<span data-ttu-id="f39c6-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f39c6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f39c6-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="f39c6-117">-Name</span></span>
<span data-ttu-id="f39c6-118">Especifica o nome do perfil do pool de agentes que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="f39c6-118">Specifies the name of the agent pool profile that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f39c6-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f39c6-119">-Confirm</span></span>
<span data-ttu-id="f39c6-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f39c6-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f39c6-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f39c6-121">-WhatIf</span></span>
<span data-ttu-id="f39c6-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f39c6-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f39c6-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f39c6-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f39c6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f39c6-124">CommonParameters</span></span>
<span data-ttu-id="f39c6-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f39c6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f39c6-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f39c6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f39c6-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f39c6-127">INPUTS</span></span>

### <span data-ttu-id="f39c6-128">ContainerService</span><span class="sxs-lookup"><span data-stu-id="f39c6-128">ContainerService</span></span>
<span data-ttu-id="f39c6-129">O parâmetro ' ContainerService ' aceita o valor do tipo ' ContainerService ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="f39c6-129">Parameter 'ContainerService' accepts value of type 'ContainerService' from the pipeline</span></span>

## <span data-ttu-id="f39c6-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f39c6-130">OUTPUTS</span></span>

### <span data-ttu-id="f39c6-131">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="f39c6-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="f39c6-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f39c6-132">NOTES</span></span>

## <span data-ttu-id="f39c6-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f39c6-133">RELATED LINKS</span></span>

[<span data-ttu-id="f39c6-134">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="f39c6-134">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="f39c6-135">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="f39c6-135">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)


