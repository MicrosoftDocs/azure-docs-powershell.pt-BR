---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: ED37B17D-C513-422A-89EA-A6AF1C9A5FEE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmContainerServiceAgentPoolProfile.md
ms.openlocfilehash: cfcb3c7657bc0ff99646c3ef21eb5cceb592fe2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602165"
---
# <span data-ttu-id="0fa40-101">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="0fa40-101">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="0fa40-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0fa40-102">SYNOPSIS</span></span>
<span data-ttu-id="0fa40-103">Remove um perfil de pool de agente de um serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="0fa40-103">Removes an agent pool profile from a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0fa40-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0fa40-104">SYNTAX</span></span>

```
Remove-AzureRmContainerServiceAgentPoolProfile [-ContainerService] <ContainerService> [-Name] <String>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fa40-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0fa40-105">DESCRIPTION</span></span>
<span data-ttu-id="0fa40-106">O cmdlet **Remove-AzureRmContainerServiceAgentPoolProfile** remove um perfil de pool de agente de um serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="0fa40-106">The **Remove-AzureRmContainerServiceAgentPoolProfile** cmdlet removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="0fa40-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0fa40-107">EXAMPLES</span></span>

### <span data-ttu-id="0fa40-108">Exemplo 1: remover um perfil de um serviço de contêiner</span><span class="sxs-lookup"><span data-stu-id="0fa40-108">Example 1: Remove a profile from a container service</span></span>
```
PS C:\> $Container = Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" 
PS C:\> Remove-AzureRmContainerServiceAgentPoolProfile -ContainerService $Container -Name "AgentPool01"
```

<span data-ttu-id="0fa40-109">O primeiro comando obtém um serviço de contêiner chamado CSResourceGroup17 usando o cmdlet Get-AzureRmContainerService.</span><span class="sxs-lookup"><span data-stu-id="0fa40-109">The first command gets a container service named CSResourceGroup17 by using the Get-AzureRmContainerService cmdlet.</span></span>
<span data-ttu-id="0fa40-110">O comando armazena o serviço na variável $Container.</span><span class="sxs-lookup"><span data-stu-id="0fa40-110">The command stores the service in the $Container variable.</span></span>

<span data-ttu-id="0fa40-111">O segundo comando Remove o perfil chamado AgentPool01 do serviço de contêiner em $Container.</span><span class="sxs-lookup"><span data-stu-id="0fa40-111">The second command removes the profile named AgentPool01 from the container service in $Container.</span></span>

## <span data-ttu-id="0fa40-112">OS</span><span class="sxs-lookup"><span data-stu-id="0fa40-112">PARAMETERS</span></span>

### <span data-ttu-id="0fa40-113">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="0fa40-113">-ContainerService</span></span>
<span data-ttu-id="0fa40-114">Especifica o objeto de serviço de contêiner do qual esse cmdlet Remove um perfil de pool do agente.</span><span class="sxs-lookup"><span data-stu-id="0fa40-114">Specifies the container service object from which this cmdlet removes an agent pool profile.</span></span>

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

### <span data-ttu-id="0fa40-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="0fa40-115">-Name</span></span>
<span data-ttu-id="0fa40-116">Especifica o nome do perfil do pool de agentes que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="0fa40-116">Specifies the name of the agent pool profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0fa40-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0fa40-117">-Confirm</span></span>
<span data-ttu-id="0fa40-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0fa40-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fa40-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fa40-119">-WhatIf</span></span>
<span data-ttu-id="0fa40-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0fa40-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0fa40-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0fa40-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fa40-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fa40-122">CommonParameters</span></span>
<span data-ttu-id="0fa40-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fa40-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fa40-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fa40-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fa40-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0fa40-125">INPUTS</span></span>

### <span data-ttu-id="0fa40-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="0fa40-126">None</span></span>
<span data-ttu-id="0fa40-127">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="0fa40-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0fa40-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0fa40-128">OUTPUTS</span></span>

## <span data-ttu-id="0fa40-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0fa40-129">NOTES</span></span>

## <span data-ttu-id="0fa40-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0fa40-130">RELATED LINKS</span></span>

[<span data-ttu-id="0fa40-131">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="0fa40-131">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="0fa40-132">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="0fa40-132">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)


