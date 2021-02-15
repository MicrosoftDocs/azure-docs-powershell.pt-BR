---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAdaptiveApplicationControlGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControlGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControlGroup.md
ms.openlocfilehash: 9d36169439a2466ca50858f5b438822461259cf3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114522"
---
# <span data-ttu-id="14a83-101">Get-AzSecurityAdaptiveApplicationControlGroup</span><span class="sxs-lookup"><span data-stu-id="14a83-101">Get-AzSecurityAdaptiveApplicationControlGroup</span></span>

## <span data-ttu-id="14a83-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="14a83-102">SYNOPSIS</span></span>
<span data-ttu-id="14a83-103">Obtém um grupo de VM/servidor de controle de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="14a83-103">Gets an application control VM/server group.</span></span>

## <span data-ttu-id="14a83-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="14a83-104">SYNTAX</span></span>

### <span data-ttu-id="14a83-105">SubscriptionScope (Padrão)</span><span class="sxs-lookup"><span data-stu-id="14a83-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAdaptiveApplicationControlGroup  -GroupName <String> -AscLocation <String> [-SubscriptionId <String>]
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14a83-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="14a83-106">DESCRIPTION</span></span>
<span data-ttu-id="14a83-107">Controles de Aplicativo Adaptáveis são calculados automaticamente pela Central de Segurança do Azure, use este cmdlet para obter um grupo de VM/servidor de controle de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="14a83-107">Adaptive Application Controls are automatically calculated by Azure Security Center, use this cmdlet to get an application control VM/server group.</span></span>

## <span data-ttu-id="14a83-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="14a83-108">EXAMPLES</span></span>

### <span data-ttu-id="14a83-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="14a83-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveApplicationControlGroup -GroupName GROUP1 -AscLocation centralus
Id         : /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/providers/Microsoft.Security/locations/centralus/applicationWhitelistings/GROUP1
Name       : GROUP1
Type       : Microsoft.Security/applicationWhitelistings
Location   : centralus
Properties : Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControlsProperties
```
<span data-ttu-id="14a83-110">Obtém um grupo de VM/servidor de controle de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="14a83-110">Gets an application control VM/server group.</span></span>


## <span data-ttu-id="14a83-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="14a83-111">PARAMETERS</span></span>

### <span data-ttu-id="14a83-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14a83-112">-DefaultProfile</span></span>
<span data-ttu-id="14a83-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="14a83-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14a83-114">-AscLocation</span><span class="sxs-lookup"><span data-stu-id="14a83-114">-AscLocation</span></span>
<span data-ttu-id="14a83-115">O local onde o ASC armazena os dados da assinatura.</span><span class="sxs-lookup"><span data-stu-id="14a83-115">The location where ASC stores the data of the subscription.</span></span> <span data-ttu-id="14a83-116">podem ser recuperados de Obter locais.</span><span class="sxs-lookup"><span data-stu-id="14a83-116">can be retrieved from Get locations.</span></span>

```yaml
Type: System.String
Parameter Sets: AscLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14a83-117">-GroupName</span><span class="sxs-lookup"><span data-stu-id="14a83-117">-GroupName</span></span>
<span data-ttu-id="14a83-118">Nome de um grupo VM/servidor de controle de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="14a83-118">Name of an application control VM/server group.</span></span>

```yaml
Type: System.String
Parameter Sets: GroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14a83-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="14a83-119">-SubscriptionId</span></span>
<span data-ttu-id="14a83-120">ID de assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="14a83-120">Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```


### <span data-ttu-id="14a83-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14a83-121">CommonParameters</span></span>
<span data-ttu-id="14a83-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14a83-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14a83-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14a83-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14a83-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="14a83-124">INPUTS</span></span>

### <span data-ttu-id="14a83-125">System.String</span><span class="sxs-lookup"><span data-stu-id="14a83-125">System.String</span></span>

## <span data-ttu-id="14a83-126">Saídas</span><span class="sxs-lookup"><span data-stu-id="14a83-126">OUTPUTS</span></span>

### <span data-ttu-id="14a83-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span><span class="sxs-lookup"><span data-stu-id="14a83-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span></span>

## <span data-ttu-id="14a83-128">Notas</span><span class="sxs-lookup"><span data-stu-id="14a83-128">NOTES</span></span>

## <span data-ttu-id="14a83-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="14a83-129">RELATED LINKS</span></span>