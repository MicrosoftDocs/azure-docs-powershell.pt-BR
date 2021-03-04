---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecuritySetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySetting.md
ms.openlocfilehash: 7c443625294b3a23ac79dfcbabb724a2d3fceaa3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887854"
---
# <span data-ttu-id="71fbb-101">Get-AzSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="71fbb-101">Get-AzSecuritySetting</span></span>

## <span data-ttu-id="71fbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71fbb-102">SYNOPSIS</span></span>
<span data-ttu-id="71fbb-103">Obter configurações de segurança no Centro de Segurança do Azure</span><span class="sxs-lookup"><span data-stu-id="71fbb-103">Get security settings in Azure Security Center</span></span>

## <span data-ttu-id="71fbb-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="71fbb-104">SYNTAX</span></span>

### <span data-ttu-id="71fbb-105">SubscriptionScope (Padrão)</span><span class="sxs-lookup"><span data-stu-id="71fbb-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71fbb-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="71fbb-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySetting -SettingName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71fbb-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="71fbb-107">DESCRIPTION</span></span>
<span data-ttu-id="71fbb-108">O Get-AzSecuritySetting cmdlet recebe configurações de segurança no Centro de Segurança do Azure.</span><span class="sxs-lookup"><span data-stu-id="71fbb-108">The Get-AzSecuritySetting cmdlet get security settings in Azure Security Center.</span></span>

## <span data-ttu-id="71fbb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="71fbb-109">EXAMPLES</span></span>

### <span data-ttu-id="71fbb-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="71fbb-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSecuritySetting -SettingName "MCAS"

Id: "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/settings/MCAS"
Name: "MCAS"
Type: "Microsoft.Security/settings"
Enabled: true
```

<span data-ttu-id="71fbb-111">Obtém uma configuração de exportação de dados MCAS</span><span class="sxs-lookup"><span data-stu-id="71fbb-111">Gets an MCAS data export setting</span></span>   

## <span data-ttu-id="71fbb-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="71fbb-112">PARAMETERS</span></span>

### <span data-ttu-id="71fbb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71fbb-113">-DefaultProfile</span></span>
<span data-ttu-id="71fbb-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="71fbb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71fbb-115">-SettingName</span><span class="sxs-lookup"><span data-stu-id="71fbb-115">-SettingName</span></span>
<span data-ttu-id="71fbb-116">Nome da configuração.</span><span class="sxs-lookup"><span data-stu-id="71fbb-116">Setting name.</span></span> <span data-ttu-id="71fbb-117">(MCAS/WDATP)</span><span class="sxs-lookup"><span data-stu-id="71fbb-117">(MCAS/WDATP)</span></span>

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

### <span data-ttu-id="71fbb-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71fbb-118">CommonParameters</span></span>
<span data-ttu-id="71fbb-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71fbb-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71fbb-120">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="71fbb-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71fbb-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="71fbb-121">INPUTS</span></span>

### <span data-ttu-id="71fbb-122">System.String</span><span class="sxs-lookup"><span data-stu-id="71fbb-122">System.String</span></span>

## <span data-ttu-id="71fbb-123">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="71fbb-123">OUTPUTS</span></span>

### <span data-ttu-id="71fbb-124">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="71fbb-124">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="71fbb-125">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="71fbb-125">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

## <span data-ttu-id="71fbb-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="71fbb-126">NOTES</span></span>

## <span data-ttu-id="71fbb-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="71fbb-127">RELATED LINKS</span></span>
