---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAdaptiveApplicationControlGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControlGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControlGroup.md
ms.openlocfilehash: 9d36169439a2466ca50858f5b438822461259cf3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284169"
---
# <span data-ttu-id="1eb04-101">Get-AzSecurityAdaptiveApplicationControlGroup</span><span class="sxs-lookup"><span data-stu-id="1eb04-101">Get-AzSecurityAdaptiveApplicationControlGroup</span></span>

## <span data-ttu-id="1eb04-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1eb04-102">SYNOPSIS</span></span>
<span data-ttu-id="1eb04-103">Obtém um grupo de VMs/servidor de controle de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1eb04-103">Gets an application control VM/server group.</span></span>

## <span data-ttu-id="1eb04-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1eb04-104">SYNTAX</span></span>

### <span data-ttu-id="1eb04-105">SubscriptionScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="1eb04-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAdaptiveApplicationControlGroup  -GroupName <String> -AscLocation <String> [-SubscriptionId <String>]
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1eb04-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1eb04-106">DESCRIPTION</span></span>
<span data-ttu-id="1eb04-107">Os controles de aplicativos adaptáveis são calculados automaticamente pela central de segurança do Azure, use esse cmdlet para obter um controle de aplicativo/VM/grupo de servidor.</span><span class="sxs-lookup"><span data-stu-id="1eb04-107">Adaptive Application Controls are automatically calculated by Azure Security Center, use this cmdlet to get an application control VM/server group.</span></span>

## <span data-ttu-id="1eb04-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1eb04-108">EXAMPLES</span></span>

### <span data-ttu-id="1eb04-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1eb04-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveApplicationControlGroup -GroupName GROUP1 -AscLocation centralus
Id         : /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/providers/Microsoft.Security/locations/centralus/applicationWhitelistings/GROUP1
Name       : GROUP1
Type       : Microsoft.Security/applicationWhitelistings
Location   : centralus
Properties : Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControlsProperties
```
<span data-ttu-id="1eb04-110">Obtém um grupo de VMs/servidor de controle de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1eb04-110">Gets an application control VM/server group.</span></span>


## <span data-ttu-id="1eb04-111">OS</span><span class="sxs-lookup"><span data-stu-id="1eb04-111">PARAMETERS</span></span>

### <span data-ttu-id="1eb04-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1eb04-112">-DefaultProfile</span></span>
<span data-ttu-id="1eb04-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1eb04-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1eb04-114">-AscLocation</span><span class="sxs-lookup"><span data-stu-id="1eb04-114">-AscLocation</span></span>
<span data-ttu-id="1eb04-115">O local onde o ASC armazena os dados da assinatura.</span><span class="sxs-lookup"><span data-stu-id="1eb04-115">The location where ASC stores the data of the subscription.</span></span> <span data-ttu-id="1eb04-116">pode ser recuperada de obter locais.</span><span class="sxs-lookup"><span data-stu-id="1eb04-116">can be retrieved from Get locations.</span></span>

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

### <span data-ttu-id="1eb04-117">-Nome_do_grupo</span><span class="sxs-lookup"><span data-stu-id="1eb04-117">-GroupName</span></span>
<span data-ttu-id="1eb04-118">Nome de um grupo de VM/servidor de controle de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1eb04-118">Name of an application control VM/server group.</span></span>

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

### <span data-ttu-id="1eb04-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1eb04-119">-SubscriptionId</span></span>
<span data-ttu-id="1eb04-120">ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="1eb04-120">Azure subscription ID.</span></span>

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


### <span data-ttu-id="1eb04-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1eb04-121">CommonParameters</span></span>
<span data-ttu-id="1eb04-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1eb04-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1eb04-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1eb04-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1eb04-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1eb04-124">INPUTS</span></span>

### <span data-ttu-id="1eb04-125">System. String</span><span class="sxs-lookup"><span data-stu-id="1eb04-125">System.String</span></span>

## <span data-ttu-id="1eb04-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1eb04-126">OUTPUTS</span></span>

### <span data-ttu-id="1eb04-127">Microsoft. Azure. Commands. Security. Models. AdaptiveApplicationControls. PSSecurityAdaptiveApplicationControls</span><span class="sxs-lookup"><span data-stu-id="1eb04-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span></span>

## <span data-ttu-id="1eb04-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1eb04-128">NOTES</span></span>

## <span data-ttu-id="1eb04-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1eb04-129">RELATED LINKS</span></span>