---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: 274a751130d5dba8d246a2f02f72be815f889378
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772498"
---
# <span data-ttu-id="70ac9-101">Get-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="70ac9-101">Get-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="70ac9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="70ac9-102">SYNOPSIS</span></span>
<span data-ttu-id="70ac9-103">Obtém as configurações do espaço de trabalho de segurança configurado em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="70ac9-103">Gets the configured security workspace settings on a subscription.</span></span>

## <span data-ttu-id="70ac9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="70ac9-104">SYNTAX</span></span>

### <span data-ttu-id="70ac9-105">SubscriptionScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="70ac9-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityWorkspaceSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70ac9-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="70ac9-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityWorkspaceSetting -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70ac9-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="70ac9-107">ResourceId</span></span>
```
Get-AzSecurityWorkspaceSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="70ac9-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="70ac9-108">DESCRIPTION</span></span>
<span data-ttu-id="70ac9-109">Esse cmdlet permite que você descubra o espaço de trabalho configurado que manterá os dados de segurança coletados pelo agente de segurança instalado em VMs dentro desta assinatura.</span><span class="sxs-lookup"><span data-stu-id="70ac9-109">This cmdlet lets you discover the configured workspace that will hold the security data that was collected by the security agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="70ac9-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="70ac9-110">EXAMPLES</span></span>

### <span data-ttu-id="70ac9-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="70ac9-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityWorkspaceSetting

Id                                                                                                         Name    WorkspaceId                                                                                                                               
--                                                                                                         ----    -----------                                                                                                                               
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityus...
```

<span data-ttu-id="70ac9-112">Obtém as configurações do espaço de trabalho para uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="70ac9-112">Gets the workspace settings for a subscription.</span></span>

## <span data-ttu-id="70ac9-113">OS</span><span class="sxs-lookup"><span data-stu-id="70ac9-113">PARAMETERS</span></span>

### <span data-ttu-id="70ac9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70ac9-114">-DefaultProfile</span></span>
<span data-ttu-id="70ac9-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="70ac9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70ac9-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="70ac9-116">-Name</span></span>
<span data-ttu-id="70ac9-117">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="70ac9-117">Resource name.</span></span>

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

### <span data-ttu-id="70ac9-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="70ac9-118">-ResourceId</span></span>
<span data-ttu-id="70ac9-119">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="70ac9-119">Resource ID.</span></span>

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

### <span data-ttu-id="70ac9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70ac9-120">CommonParameters</span></span>
<span data-ttu-id="70ac9-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70ac9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70ac9-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70ac9-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70ac9-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="70ac9-123">INPUTS</span></span>

### <span data-ttu-id="70ac9-124">System. String</span><span class="sxs-lookup"><span data-stu-id="70ac9-124">System.String</span></span>

## <span data-ttu-id="70ac9-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="70ac9-125">OUTPUTS</span></span>

### <span data-ttu-id="70ac9-126">Microsoft. Azure. Commands. Security. Models. WorkspaceSettings. PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="70ac9-126">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="70ac9-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="70ac9-127">NOTES</span></span>

## <span data-ttu-id="70ac9-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="70ac9-128">RELATED LINKS</span></span>
