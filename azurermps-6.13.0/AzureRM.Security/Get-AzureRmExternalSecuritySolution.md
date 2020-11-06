---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmExternalSecuritySolution.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmExternalSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmExternalSecuritySolution.md
ms.openlocfilehash: 4ef54651b5490161d7fc28c4a0c068f7b4a1ed76
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432257"
---
# <span data-ttu-id="0a6cc-101">Get-AzureRmExternalSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="0a6cc-101">Get-AzureRmExternalSecuritySolution</span></span>

## <span data-ttu-id="0a6cc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0a6cc-102">SYNOPSIS</span></span>
<span data-ttu-id="0a6cc-103">Obter solução de segurança externa</span><span class="sxs-lookup"><span data-stu-id="0a6cc-103">Get external security solution</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a6cc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0a6cc-104">SYNTAX</span></span>

### <span data-ttu-id="0a6cc-105">SubscriptionScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="0a6cc-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmExternalSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a6cc-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="0a6cc-106">ResourceGroupLevelResource</span></span>
```
Get-AzureRmExternalSecuritySolution -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a6cc-107">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="0a6cc-107">SubscriptionLevelResource</span></span>
```
Get-AzureRmExternalSecuritySolution -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0a6cc-108">Identificação</span><span class="sxs-lookup"><span data-stu-id="0a6cc-108">ResourceId</span></span>
```
Get-AzureRmExternalSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0a6cc-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0a6cc-109">DESCRIPTION</span></span>
<span data-ttu-id="0a6cc-110">Obter solução de segurança externa</span><span class="sxs-lookup"><span data-stu-id="0a6cc-110">Get external security solution</span></span>

## <span data-ttu-id="0a6cc-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0a6cc-111">EXAMPLES</span></span>

### <span data-ttu-id="0a6cc-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0a6cc-112">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmExternalSecuritySolution
ConnectivityState : Discovered
DeviceType        : Azure Active Directory Identity Protection
DeviceVendor      : microsoft
Workspace         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/defaultresourcegroup-eus/provide
                    rs/microsoft.operationalinsights/workspaces/defaultworkspace-487bb485-b5b0-471e-9c0d-10717612f869-e
                    us
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/defaultresourcegroup-eus/provide
                    rs/Microsoft.Security/locations/centralus/externalSecuritySolutions/aad_defaultworkspace-487bb485-b
                    5b0-471e-9c0d-10717612f869-eus
Name              : aad_defaultworkspace-487bb485-b5b0-471e-9c0d-10717612f869-eus
Kind              : AAD

ConnectivityState : Discovered
DeviceType        : Azure Active Directory Identity Protection
DeviceVendor      : microsoft
Workspace         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/defaultresourcegroup-weu/provide
                    rs/microsoft.operationalinsights/workspaces/defaultworkspace-487bb485-b5b0-471e-9c0d-10717612f869-w
                    eu
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/defaultresourcegroup-weu/provide
                    rs/Microsoft.Security/locations/centralus/externalSecuritySolutions/aad_defaultworkspace-487bb485-b
                    5b0-471e-9c0d-10717612f869-weu
Name              : aad_defaultworkspace-487bb485-b5b0-471e-9c0d-10717612f869-weu
Kind              : AAD

ConnectivityState : Discovered
DeviceType        : Azure Active Directory Identity Protection
DeviceVendor      : microsoft
Workspace         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.opera
                    tionalinsights/workspaces/securityuserws
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/mainws/providers/Microsoft.Secur
                    ity/locations/centralus/externalSecuritySolutions/aad_securityuserws
Name              : aad_securityuserws
Kind              : AAD

ConnectivityState : Discovered
DeviceType        : Azure Active Directory Identity Protection
DeviceVendor      : microsoft
Workspace         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/myservice1/providers/microsoft.o
                    perationalinsights/workspaces/testservicews
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myservice1/providers/Microsoft.S
                    ecurity/locations/centralus/externalSecuritySolutions/aad_testservicews
Name              : aad_testservicews
Kind              : AAD
```

<span data-ttu-id="0a6cc-113">Obter todas as soluções de segurança externa na assinatura</span><span class="sxs-lookup"><span data-stu-id="0a6cc-113">Get all the external security solutions in the subscription</span></span>

### <span data-ttu-id="0a6cc-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="0a6cc-114">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmExternalSecuritySolution -ResourceGroupName "myservice1" -Location "centralus" -Name "aad_testservicews"
ConnectivityState : Discovered
DeviceType        : Azure Active Directory Identity Protection
DeviceVendor      : microsoft
Workspace         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/myservice1/providers/microsoft.operationalinsights/workspaces/testservicews
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myservice1/providers/Microsoft.Security/locations/centralus/externalSecuritySolutions/aad_testservicews
Name              : aad_testservicews
Kind              : AAD
```

<span data-ttu-id="0a6cc-115">Obter uma solução de segurança externa específica</span><span class="sxs-lookup"><span data-stu-id="0a6cc-115">Get a specific external security solution</span></span>

## <span data-ttu-id="0a6cc-116">OS</span><span class="sxs-lookup"><span data-stu-id="0a6cc-116">PARAMETERS</span></span>

### <span data-ttu-id="0a6cc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a6cc-117">-DefaultProfile</span></span>
<span data-ttu-id="0a6cc-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0a6cc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a6cc-119">-Local</span><span class="sxs-lookup"><span data-stu-id="0a6cc-119">-Location</span></span>
<span data-ttu-id="0a6cc-120">Ponto.</span><span class="sxs-lookup"><span data-stu-id="0a6cc-120">Location.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource, SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a6cc-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="0a6cc-121">-Name</span></span>
<span data-ttu-id="0a6cc-122">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="0a6cc-122">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a6cc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a6cc-123">-ResourceGroupName</span></span>
<span data-ttu-id="0a6cc-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0a6cc-124">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a6cc-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a6cc-125">-ResourceId</span></span>
<span data-ttu-id="0a6cc-126">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="0a6cc-126">Resource ID.</span></span>

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

### <span data-ttu-id="0a6cc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a6cc-127">CommonParameters</span></span>
<span data-ttu-id="0a6cc-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a6cc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a6cc-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a6cc-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a6cc-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0a6cc-130">INPUTS</span></span>

### <span data-ttu-id="0a6cc-131">System. String</span><span class="sxs-lookup"><span data-stu-id="0a6cc-131">System.String</span></span>

## <span data-ttu-id="0a6cc-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0a6cc-132">OUTPUTS</span></span>

### <span data-ttu-id="0a6cc-133">Microsoft. Azure. Commands. Security. Models. ExternalSecuritySolutions. PSSecurityExternalSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="0a6cc-133">Microsoft.Azure.Commands.Security.Models.ExternalSecuritySolutions.PSSecurityExternalSecuritySolution</span></span>

## <span data-ttu-id="0a6cc-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0a6cc-134">NOTES</span></span>

## <span data-ttu-id="0a6cc-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0a6cc-135">RELATED LINKS</span></span>
