---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: f0de174ac85fb4247ac8af55f8a8ab9cb64d6446
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888074"
---
# <span data-ttu-id="17735-101">Get-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="17735-101">Get-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="17735-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17735-102">SYNOPSIS</span></span>
<span data-ttu-id="17735-103">Obtém as configurações de espaço de trabalho de segurança em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="17735-103">Gets the configured security workspace settings on a subscription.</span></span>

## <span data-ttu-id="17735-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="17735-104">SYNTAX</span></span>

### <span data-ttu-id="17735-105">SubscriptionScope (Padrão)</span><span class="sxs-lookup"><span data-stu-id="17735-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityWorkspaceSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17735-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="17735-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityWorkspaceSetting -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17735-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="17735-107">ResourceId</span></span>
```
Get-AzSecurityWorkspaceSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="17735-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="17735-108">DESCRIPTION</span></span>
<span data-ttu-id="17735-109">Este cmdlet permite que você descubra o espaço de trabalho configurado que manterá os dados de segurança coletados pelo agente de segurança que está instalado em VMs dentro dessa assinatura.</span><span class="sxs-lookup"><span data-stu-id="17735-109">This cmdlet lets you discover the configured workspace that will hold the security data that was collected by the security agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="17735-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="17735-110">EXAMPLES</span></span>

### <span data-ttu-id="17735-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="17735-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityWorkspaceSetting

Id                                                                                                         Name    WorkspaceId                                                                                                                               
--                                                                                                         ----    -----------                                                                                                                               
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityus...
```

<span data-ttu-id="17735-112">Obtém as configurações de espaço de trabalho para uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="17735-112">Gets the workspace settings for a subscription.</span></span>

## <span data-ttu-id="17735-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="17735-113">PARAMETERS</span></span>

### <span data-ttu-id="17735-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17735-114">-DefaultProfile</span></span>
<span data-ttu-id="17735-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="17735-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17735-116">-Name</span><span class="sxs-lookup"><span data-stu-id="17735-116">-Name</span></span>
<span data-ttu-id="17735-117">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="17735-117">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17735-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="17735-118">-ResourceId</span></span>
<span data-ttu-id="17735-119">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="17735-119">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17735-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17735-120">CommonParameters</span></span>
<span data-ttu-id="17735-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17735-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17735-122">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17735-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17735-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="17735-123">INPUTS</span></span>

### <span data-ttu-id="17735-124">System.String</span><span class="sxs-lookup"><span data-stu-id="17735-124">System.String</span></span>

## <span data-ttu-id="17735-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="17735-125">OUTPUTS</span></span>

### <span data-ttu-id="17735-126">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="17735-126">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="17735-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="17735-127">NOTES</span></span>

## <span data-ttu-id="17735-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="17735-128">RELATED LINKS</span></span>
