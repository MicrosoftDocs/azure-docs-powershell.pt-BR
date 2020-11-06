---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 6140E973-D7AB-4A28-A4FA-818E08129372
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermautoscalesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAutoscaleSetting.md
ms.openlocfilehash: 4d6c2f748915847038ef4029dc024763375ef99e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428924"
---
# <span data-ttu-id="10cb8-101">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="10cb8-101">Remove-AzureRmAutoscaleSetting</span></span>

## <span data-ttu-id="10cb8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="10cb8-102">SYNOPSIS</span></span>
<span data-ttu-id="10cb8-103">Remove uma configuração de autoescala.</span><span class="sxs-lookup"><span data-stu-id="10cb8-103">Removes an Autoscale setting.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10cb8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="10cb8-104">SYNTAX</span></span>

```
Remove-AzureRmAutoscaleSetting -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10cb8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="10cb8-105">DESCRIPTION</span></span>
<span data-ttu-id="10cb8-106">O cmdlet **Remove-AzureRmAutoscaleSetting** remove uma configuração de autoescala.</span><span class="sxs-lookup"><span data-stu-id="10cb8-106">The **Remove-AzureRmAutoscaleSetting** cmdlet removes an Autoscale setting.</span></span>
<span data-ttu-id="10cb8-107">Você deve especificar o nome da configuração e o nome do grupo de recursos ao qual ele está atribuído.</span><span class="sxs-lookup"><span data-stu-id="10cb8-107">You must specify the name of the setting and the name of the resource group to which it is assigned.</span></span>

<span data-ttu-id="10cb8-108">Esse cmdlet implementa o padrão ShouldProcess, ou seja, ele pode solicitar confirmação do usuário antes de realmente criar, modificar ou remover o recurso.</span><span class="sxs-lookup"><span data-stu-id="10cb8-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="10cb8-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="10cb8-109">EXAMPLES</span></span>

## <span data-ttu-id="10cb8-110">OS</span><span class="sxs-lookup"><span data-stu-id="10cb8-110">PARAMETERS</span></span>

### <span data-ttu-id="10cb8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10cb8-111">-DefaultProfile</span></span>
<span data-ttu-id="10cb8-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="10cb8-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="10cb8-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="10cb8-113">-Name</span></span>
<span data-ttu-id="10cb8-114">Especifica o nome da configuração de dimensionamento automático a ser removida.</span><span class="sxs-lookup"><span data-stu-id="10cb8-114">Specifies the name of the Autoscale setting to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10cb8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10cb8-115">-ResourceGroupName</span></span>
<span data-ttu-id="10cb8-116">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="10cb8-116">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10cb8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10cb8-117">CommonParameters</span></span>
<span data-ttu-id="10cb8-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10cb8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10cb8-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10cb8-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10cb8-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="10cb8-120">INPUTS</span></span>

### <span data-ttu-id="10cb8-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="10cb8-121">None</span></span>
<span data-ttu-id="10cb8-122">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="10cb8-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="10cb8-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="10cb8-123">OUTPUTS</span></span>

### <span data-ttu-id="10cb8-124">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="10cb8-124">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="10cb8-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="10cb8-125">NOTES</span></span>

## <span data-ttu-id="10cb8-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="10cb8-126">RELATED LINKS</span></span>

[<span data-ttu-id="10cb8-127">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="10cb8-127">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="10cb8-128">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="10cb8-128">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)


