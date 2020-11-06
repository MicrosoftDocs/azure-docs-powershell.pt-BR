---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityWorkspaceSetting.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityWorkspaceSetting.md
ms.openlocfilehash: 7e2a655810c885245d3694fb63caa44c5b4119e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602902"
---
# <span data-ttu-id="3e857-101">Get-AzureRmSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="3e857-101">Get-AzureRmSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="3e857-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3e857-102">SYNOPSIS</span></span>
<span data-ttu-id="3e857-103">Obtém as configurações do espaço de trabalho de segurança configurado em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="3e857-103">Gets the configured security workspace settings on a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e857-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3e857-104">SYNTAX</span></span>

### <span data-ttu-id="3e857-105">SubscriptionScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="3e857-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmSecurityWorkspaceSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e857-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="3e857-106">SubscriptionLevelResource</span></span>
```
Get-AzureRmSecurityWorkspaceSetting -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3e857-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="3e857-107">ResourceId</span></span>
```
Get-AzureRmSecurityWorkspaceSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3e857-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3e857-108">DESCRIPTION</span></span>
<span data-ttu-id="3e857-109">Esse cmdlet permite que você descubra o espaço de trabalho configurado que manterá os dados de segurança coletados pelo agente de segurança instalado em VMs dentro desta assinatura.</span><span class="sxs-lookup"><span data-stu-id="3e857-109">This cmdlet lets you discover the configured workspace that will hold the security data that was collected by the security agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="3e857-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3e857-110">EXAMPLES</span></span>

### <span data-ttu-id="3e857-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3e857-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSecurityWorkspaceSetting

Id                                                                                                         Name    WorkspaceId                                                                                                                               
--                                                                                                         ----    -----------                                                                                                                               
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityus...
```

<span data-ttu-id="3e857-112">Obtém as configurações do espaço de trabalho para uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="3e857-112">Gets the workspace settings for a subscription.</span></span>

## <span data-ttu-id="3e857-113">OS</span><span class="sxs-lookup"><span data-stu-id="3e857-113">PARAMETERS</span></span>

### <span data-ttu-id="3e857-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e857-114">-DefaultProfile</span></span>
<span data-ttu-id="3e857-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3e857-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e857-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="3e857-116">-Name</span></span>
<span data-ttu-id="3e857-117">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="3e857-117">Resource name.</span></span>

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

### <span data-ttu-id="3e857-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e857-118">-ResourceId</span></span>
<span data-ttu-id="3e857-119">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="3e857-119">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e857-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e857-120">CommonParameters</span></span>
<span data-ttu-id="3e857-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e857-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e857-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e857-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e857-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3e857-123">INPUTS</span></span>

### <span data-ttu-id="3e857-124">System. String</span><span class="sxs-lookup"><span data-stu-id="3e857-124">System.String</span></span>

## <span data-ttu-id="3e857-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3e857-125">OUTPUTS</span></span>

### <span data-ttu-id="3e857-126">Microsoft. Azure. Commands. Security. Models. WorkspaceSettings. PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="3e857-126">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="3e857-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3e857-127">NOTES</span></span>

## <span data-ttu-id="3e857-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3e857-128">RELATED LINKS</span></span>
