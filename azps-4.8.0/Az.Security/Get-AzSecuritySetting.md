---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySetting.md
ms.openlocfilehash: 708fb6b3807e874d00c3e555ef84973572edcd1c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110904"
---
# <span data-ttu-id="c42e8-101">Get-AzSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="c42e8-101">Get-AzSecuritySetting</span></span>

## <span data-ttu-id="c42e8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c42e8-102">SYNOPSIS</span></span>
<span data-ttu-id="c42e8-103">Obter configurações de segurança na central de segurança do Azure</span><span class="sxs-lookup"><span data-stu-id="c42e8-103">Get security settings in Azure Security Center</span></span>

## <span data-ttu-id="c42e8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c42e8-104">SYNTAX</span></span>

### <span data-ttu-id="c42e8-105">SubscriptionScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="c42e8-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c42e8-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="c42e8-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySetting -SettingName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c42e8-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c42e8-107">DESCRIPTION</span></span>
<span data-ttu-id="c42e8-108">O cmdlet Get-AzSecuritySetting obter configurações de segurança na central de segurança do Azure.</span><span class="sxs-lookup"><span data-stu-id="c42e8-108">The Get-AzSecuritySetting cmdlet get security settings in Azure Security Center.</span></span>

## <span data-ttu-id="c42e8-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c42e8-109">EXAMPLES</span></span>

### <span data-ttu-id="c42e8-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c42e8-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSecuritySetting -SettingName "MCAS"

Id: "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/settings/MCAS"
Name: "MCAS"
Type: "Microsoft.Security/settings"
Enabled: true
```

<span data-ttu-id="c42e8-111">Obtém uma configuração de exportação de dados do MCAS</span><span class="sxs-lookup"><span data-stu-id="c42e8-111">Gets an MCAS data export setting</span></span>   

## <span data-ttu-id="c42e8-112">OS</span><span class="sxs-lookup"><span data-stu-id="c42e8-112">PARAMETERS</span></span>

### <span data-ttu-id="c42e8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c42e8-113">-DefaultProfile</span></span>
<span data-ttu-id="c42e8-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c42e8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c42e8-115">-SettingName</span><span class="sxs-lookup"><span data-stu-id="c42e8-115">-SettingName</span></span>
<span data-ttu-id="c42e8-116">Nome da configuração.</span><span class="sxs-lookup"><span data-stu-id="c42e8-116">Setting name.</span></span> <span data-ttu-id="c42e8-117">(MCAS/WDATP)</span><span class="sxs-lookup"><span data-stu-id="c42e8-117">(MCAS/WDATP)</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c42e8-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c42e8-118">CommonParameters</span></span>
<span data-ttu-id="c42e8-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c42e8-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c42e8-120">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c42e8-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c42e8-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c42e8-121">INPUTS</span></span>

### <span data-ttu-id="c42e8-122">System. String</span><span class="sxs-lookup"><span data-stu-id="c42e8-122">System.String</span></span>

## <span data-ttu-id="c42e8-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c42e8-123">OUTPUTS</span></span>

### <span data-ttu-id="c42e8-124">Microsoft. Azure. Commands. Security. Models. Settings. PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="c42e8-124">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="c42e8-125">Microsoft. Azure. Commands. Security. Models. Settings. PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="c42e8-125">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

## <span data-ttu-id="c42e8-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c42e8-126">NOTES</span></span>

## <span data-ttu-id="c42e8-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c42e8-127">RELATED LINKS</span></span>
