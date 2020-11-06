---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorrulegroupoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorRuleGroupOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorRuleGroupOverrideObject.md
ms.openlocfilehash: 02253a59a7f05bfdecd8147325575605334f13ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426345"
---
# <span data-ttu-id="b3c39-101">New-AzureRmFrontDoorRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="b3c39-101">New-AzureRmFrontDoorRuleGroupOverrideObject</span></span>

## <span data-ttu-id="b3c39-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b3c39-102">SYNOPSIS</span></span>
<span data-ttu-id="b3c39-103">Criar objeto RuleGroupOverride para criação de política WAF</span><span class="sxs-lookup"><span data-stu-id="b3c39-103">Create RuleGroupOverride Object for WAF policy creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3c39-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b3c39-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorRuleGroupOverrideObject -Override <PSRuleGroupOverride> -Action <PSAction>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3c39-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b3c39-105">DESCRIPTION</span></span>
<span data-ttu-id="b3c39-106">Criar objeto RuleGroupOverride para criação de política WAF</span><span class="sxs-lookup"><span data-stu-id="b3c39-106">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="b3c39-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b3c39-107">EXAMPLES</span></span>

### <span data-ttu-id="b3c39-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b3c39-108">Example 1</span></span>
```powershell
PS C:\>  New-AzureRmFrontDoorRuleGroupOverrideObject -Override SqlInjection -Action Block

Action RuleGroupOverride
------ -----------------
 Block      SqlInjection
```

<span data-ttu-id="b3c39-109">Criar um objeto RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="b3c39-109">Create a RuleGroupOverride Object</span></span>

## <span data-ttu-id="b3c39-110">OS</span><span class="sxs-lookup"><span data-stu-id="b3c39-110">PARAMETERS</span></span>

### <span data-ttu-id="b3c39-111">-Ação</span><span class="sxs-lookup"><span data-stu-id="b3c39-111">-Action</span></span>
<span data-ttu-id="b3c39-112">Tipo de ações.</span><span class="sxs-lookup"><span data-stu-id="b3c39-112">Type of Actions.</span></span>
<span data-ttu-id="b3c39-113">Os valores possíveis incluem: ' Allow ', ' Block ', ' log '</span><span class="sxs-lookup"><span data-stu-id="b3c39-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAction
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Block, Log

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3c39-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3c39-114">-DefaultProfile</span></span>
<span data-ttu-id="b3c39-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b3c39-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3c39-116">-Substituir</span><span class="sxs-lookup"><span data-stu-id="b3c39-116">-Override</span></span>
<span data-ttu-id="b3c39-117">Descreve overrideruleGroup.</span><span class="sxs-lookup"><span data-stu-id="b3c39-117">Describes overrideruleGroup.</span></span>
<span data-ttu-id="b3c39-118">Os valores possíveis incluem: ' sqlinjeção ', ' XSS '</span><span class="sxs-lookup"><span data-stu-id="b3c39-118">Possible values include: 'SqlInjection', 'XSS'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRuleGroupOverride
Parameter Sets: (All)
Aliases:
Accepted values: SqlInjection, XSS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3c39-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3c39-119">CommonParameters</span></span>
<span data-ttu-id="b3c39-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3c39-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3c39-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3c39-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3c39-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b3c39-122">INPUTS</span></span>

### <span data-ttu-id="b3c39-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="b3c39-123">None</span></span>

## <span data-ttu-id="b3c39-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b3c39-124">OUTPUTS</span></span>

### <span data-ttu-id="b3c39-125">Microsoft. Azure. Commands. FrontDoor. Models. PSAzureRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="b3c39-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride</span></span>

## <span data-ttu-id="b3c39-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b3c39-126">NOTES</span></span>

## <span data-ttu-id="b3c39-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b3c39-127">RELATED LINKS</span></span>

[<span data-ttu-id="b3c39-128">New-AzureRmFrontDoorManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="b3c39-128">New-AzureRmFrontDoorManagedRuleObject</span></span>](./New-AzureRmFrontDoorManagedRuleObject.md)
