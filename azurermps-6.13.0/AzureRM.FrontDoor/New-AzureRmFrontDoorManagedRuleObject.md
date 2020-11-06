---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoormanagedruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorManagedRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorManagedRuleObject.md
ms.openlocfilehash: 236cb9ff263f97ae52ea5d3226f4defec00c662a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602930"
---
# <span data-ttu-id="0dda2-101">New-AzureRmFrontDoorManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="0dda2-101">New-AzureRmFrontDoorManagedRuleObject</span></span>

## <span data-ttu-id="0dda2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0dda2-102">SYNOPSIS</span></span>
<span data-ttu-id="0dda2-103">Criar objeto ManagedRule para criação de política WAF</span><span class="sxs-lookup"><span data-stu-id="0dda2-103">Create ManagedRule Object for WAF policy creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0dda2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0dda2-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorManagedRuleObject -Priority <Int32> [-Version <String>]
 [-RuleGroupOverride <PSAzureRuleGroupOverride[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0dda2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0dda2-105">DESCRIPTION</span></span>
<span data-ttu-id="0dda2-106">Criar objeto ManagedRule para criação de política WAF</span><span class="sxs-lookup"><span data-stu-id="0dda2-106">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="0dda2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0dda2-107">EXAMPLES</span></span>

### <span data-ttu-id="0dda2-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0dda2-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmFrontDoor
ManagedRuleObject -Priority 1 -Version 0 -RuleGroupOverride $override1

RuleGroupOverrides                                                   Priority Version
------------------                                                   -------- -------
{Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride}        1 0
```

<span data-ttu-id="0dda2-109">Criar um objeto ManagedRule</span><span class="sxs-lookup"><span data-stu-id="0dda2-109">Create a ManagedRule Object</span></span>

## <span data-ttu-id="0dda2-110">OS</span><span class="sxs-lookup"><span data-stu-id="0dda2-110">PARAMETERS</span></span>

### <span data-ttu-id="0dda2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dda2-111">-DefaultProfile</span></span>
<span data-ttu-id="0dda2-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0dda2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0dda2-113">-Priority</span><span class="sxs-lookup"><span data-stu-id="0dda2-113">-Priority</span></span>
<span data-ttu-id="0dda2-114">Descreve a prioridade da regra</span><span class="sxs-lookup"><span data-stu-id="0dda2-114">Describes priority of the rule</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dda2-115">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="0dda2-115">-RuleGroupOverride</span></span>
<span data-ttu-id="0dda2-116">Lista de configurações de substituição do provedor gerenciado do Azure</span><span class="sxs-lookup"><span data-stu-id="0dda2-116">List of azure managed provider override configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dda2-117">-Versão</span><span class="sxs-lookup"><span data-stu-id="0dda2-117">-Version</span></span>
<span data-ttu-id="0dda2-118">Versão do RuleSet</span><span class="sxs-lookup"><span data-stu-id="0dda2-118">Version of the ruleset</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dda2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dda2-119">CommonParameters</span></span>
<span data-ttu-id="0dda2-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0dda2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dda2-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0dda2-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dda2-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0dda2-122">INPUTS</span></span>

### <span data-ttu-id="0dda2-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="0dda2-123">None</span></span>

## <span data-ttu-id="0dda2-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0dda2-124">OUTPUTS</span></span>

### <span data-ttu-id="0dda2-125">Microsoft. Azure. Commands. FrontDoor. Models. PSAzureManagedRule</span><span class="sxs-lookup"><span data-stu-id="0dda2-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span></span>

## <span data-ttu-id="0dda2-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0dda2-126">NOTES</span></span>

## <span data-ttu-id="0dda2-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0dda2-127">RELATED LINKS</span></span>

<span data-ttu-id="0dda2-128">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md) 
 [Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md) 
 [New-AzureRmFrontDoorRuleGroupOverrideObject](./Set-AzureRmFrontDoorRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="0dda2-128">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md)
[Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md)
[New-AzureRmFrontDoorRuleGroupOverrideObject](./Set-AzureRmFrontDoorRuleGroupOverrideObject.md)</span></span>
