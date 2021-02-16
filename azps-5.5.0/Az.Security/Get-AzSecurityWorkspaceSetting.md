---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: ca4f0d39b0023d641e2f95ceb4eddf90f19a51f1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116399"
---
# <span data-ttu-id="204a9-101">Get-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="204a9-101">Get-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="204a9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="204a9-102">SYNOPSIS</span></span>
<span data-ttu-id="204a9-103">Obtém as configurações configuradas de espaço de trabalho de segurança em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="204a9-103">Gets the configured security workspace settings on a subscription.</span></span>

## <span data-ttu-id="204a9-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="204a9-104">SYNTAX</span></span>

### <span data-ttu-id="204a9-105">SubscriptionScope (Padrão)</span><span class="sxs-lookup"><span data-stu-id="204a9-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityWorkspaceSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="204a9-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="204a9-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityWorkspaceSetting -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="204a9-107">Resourceid</span><span class="sxs-lookup"><span data-stu-id="204a9-107">ResourceId</span></span>
```
Get-AzSecurityWorkspaceSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="204a9-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="204a9-108">DESCRIPTION</span></span>
<span data-ttu-id="204a9-109">Esse cmdlet permite descobrir o espaço de trabalho configurado que conterá os dados de segurança coletados pelo agente de segurança instalado em VMs dentro desta assinatura.</span><span class="sxs-lookup"><span data-stu-id="204a9-109">This cmdlet lets you discover the configured workspace that will hold the security data that was collected by the security agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="204a9-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="204a9-110">EXAMPLES</span></span>

### <span data-ttu-id="204a9-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="204a9-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityWorkspaceSetting

Id                                                                                                         Name    WorkspaceId                                                                                                                               
--                                                                                                         ----    -----------                                                                                                                               
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityus...
```

<span data-ttu-id="204a9-112">Obtém as configurações de espaço de trabalho de uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="204a9-112">Gets the workspace settings for a subscription.</span></span>

## <span data-ttu-id="204a9-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="204a9-113">PARAMETERS</span></span>

### <span data-ttu-id="204a9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="204a9-114">-DefaultProfile</span></span>
<span data-ttu-id="204a9-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="204a9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="204a9-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="204a9-116">-Name</span></span>
<span data-ttu-id="204a9-117">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="204a9-117">Resource name.</span></span>

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

### <span data-ttu-id="204a9-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="204a9-118">-ResourceId</span></span>
<span data-ttu-id="204a9-119">ID do Recurso.</span><span class="sxs-lookup"><span data-stu-id="204a9-119">Resource ID.</span></span>

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

### <span data-ttu-id="204a9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="204a9-120">CommonParameters</span></span>
<span data-ttu-id="204a9-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="204a9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="204a9-122">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="204a9-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="204a9-123">Entradas</span><span class="sxs-lookup"><span data-stu-id="204a9-123">INPUTS</span></span>

### <span data-ttu-id="204a9-124">System.String</span><span class="sxs-lookup"><span data-stu-id="204a9-124">System.String</span></span>

## <span data-ttu-id="204a9-125">Saídas</span><span class="sxs-lookup"><span data-stu-id="204a9-125">OUTPUTS</span></span>

### <span data-ttu-id="204a9-126">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="204a9-126">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="204a9-127">Notas</span><span class="sxs-lookup"><span data-stu-id="204a9-127">NOTES</span></span>

## <span data-ttu-id="204a9-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="204a9-128">RELATED LINKS</span></span>
