---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySetting.md
ms.openlocfilehash: 708fb6b3807e874d00c3e555ef84973572edcd1c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114001"
---
# <span data-ttu-id="7ed5f-101">Get-AzSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="7ed5f-101">Get-AzSecuritySetting</span></span>

## <span data-ttu-id="7ed5f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7ed5f-102">SYNOPSIS</span></span>
<span data-ttu-id="7ed5f-103">Obter configurações de segurança no Centro de Segurança do Azure</span><span class="sxs-lookup"><span data-stu-id="7ed5f-103">Get security settings in Azure Security Center</span></span>

## <span data-ttu-id="7ed5f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7ed5f-104">SYNTAX</span></span>

### <span data-ttu-id="7ed5f-105">SubscriptionScope (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7ed5f-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ed5f-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="7ed5f-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySetting -SettingName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ed5f-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="7ed5f-107">DESCRIPTION</span></span>
<span data-ttu-id="7ed5f-108">O Get-AzSecuritySetting cmdlet recebe configurações de segurança no Centro de Segurança do Azure.</span><span class="sxs-lookup"><span data-stu-id="7ed5f-108">The Get-AzSecuritySetting cmdlet get security settings in Azure Security Center.</span></span>

## <span data-ttu-id="7ed5f-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7ed5f-109">EXAMPLES</span></span>

### <span data-ttu-id="7ed5f-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7ed5f-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSecuritySetting -SettingName "MCAS"

Id: "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/settings/MCAS"
Name: "MCAS"
Type: "Microsoft.Security/settings"
Enabled: true
```

<span data-ttu-id="7ed5f-111">Obtém uma configuração de exportação de dados MCAS</span><span class="sxs-lookup"><span data-stu-id="7ed5f-111">Gets an MCAS data export setting</span></span>   

## <span data-ttu-id="7ed5f-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7ed5f-112">PARAMETERS</span></span>

### <span data-ttu-id="7ed5f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ed5f-113">-DefaultProfile</span></span>
<span data-ttu-id="7ed5f-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7ed5f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ed5f-115">-SettingName</span><span class="sxs-lookup"><span data-stu-id="7ed5f-115">-SettingName</span></span>
<span data-ttu-id="7ed5f-116">Nome da configuração.</span><span class="sxs-lookup"><span data-stu-id="7ed5f-116">Setting name.</span></span> <span data-ttu-id="7ed5f-117">(MCAS/WDATP)</span><span class="sxs-lookup"><span data-stu-id="7ed5f-117">(MCAS/WDATP)</span></span>

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

### <span data-ttu-id="7ed5f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ed5f-118">CommonParameters</span></span>
<span data-ttu-id="7ed5f-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ed5f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ed5f-120">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7ed5f-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ed5f-121">Entradas</span><span class="sxs-lookup"><span data-stu-id="7ed5f-121">INPUTS</span></span>

### <span data-ttu-id="7ed5f-122">System.String</span><span class="sxs-lookup"><span data-stu-id="7ed5f-122">System.String</span></span>

## <span data-ttu-id="7ed5f-123">Saídas</span><span class="sxs-lookup"><span data-stu-id="7ed5f-123">OUTPUTS</span></span>

### <span data-ttu-id="7ed5f-124">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="7ed5f-124">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="7ed5f-125">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="7ed5f-125">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

## <span data-ttu-id="7ed5f-126">Notas</span><span class="sxs-lookup"><span data-stu-id="7ed5f-126">NOTES</span></span>

## <span data-ttu-id="7ed5f-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7ed5f-127">RELATED LINKS</span></span>
