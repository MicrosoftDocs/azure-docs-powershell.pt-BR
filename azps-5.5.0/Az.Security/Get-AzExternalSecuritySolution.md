---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzExternalSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzExternalSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzExternalSecuritySolution.md
ms.openlocfilehash: 0314a7e6b661b0b007ffe2cf59f5618247e4b282
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116204"
---
# <span data-ttu-id="23cc1-101">Get-AzExternalSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="23cc1-101">Get-AzExternalSecuritySolution</span></span>

## <span data-ttu-id="23cc1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="23cc1-102">SYNOPSIS</span></span>
<span data-ttu-id="23cc1-103">Obter solução de segurança externa</span><span class="sxs-lookup"><span data-stu-id="23cc1-103">Get external security solution</span></span> 

## <span data-ttu-id="23cc1-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="23cc1-104">SYNTAX</span></span>

### <span data-ttu-id="23cc1-105">SubscriptionScope (Padrão)</span><span class="sxs-lookup"><span data-stu-id="23cc1-105">SubscriptionScope (Default)</span></span>
```
Get-AzExternalSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23cc1-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="23cc1-106">ResourceGroupLevelResource</span></span>
```
Get-AzExternalSecuritySolution -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23cc1-107">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="23cc1-107">SubscriptionLevelResource</span></span>
```
Get-AzExternalSecuritySolution -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="23cc1-108">Resourceid</span><span class="sxs-lookup"><span data-stu-id="23cc1-108">ResourceId</span></span>
```
Get-AzExternalSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="23cc1-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="23cc1-109">DESCRIPTION</span></span>
<span data-ttu-id="23cc1-110">Obter solução de segurança externa</span><span class="sxs-lookup"><span data-stu-id="23cc1-110">Get external security solution</span></span>

## <span data-ttu-id="23cc1-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="23cc1-111">EXAMPLES</span></span>

### <span data-ttu-id="23cc1-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="23cc1-112">Example 1</span></span>
```powershell
PS C:\> Get-AzExternalSecuritySolution
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

<span data-ttu-id="23cc1-113">Obter todas as soluções de segurança externa na assinatura</span><span class="sxs-lookup"><span data-stu-id="23cc1-113">Get all the external security solutions in the subscription</span></span>

### <span data-ttu-id="23cc1-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="23cc1-114">Example 2</span></span>
```powershell
PS C:\> Get-AzExternalSecuritySolution -ResourceGroupName "myservice1" -Location "centralus" -Name "aad_testservicews"
ConnectivityState : Discovered
DeviceType        : Azure Active Directory Identity Protection
DeviceVendor      : microsoft
Workspace         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/myservice1/providers/microsoft.operationalinsights/workspaces/testservicews
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myservice1/providers/Microsoft.Security/locations/centralus/externalSecuritySolutions/aad_testservicews
Name              : aad_testservicews
Kind              : AAD
```

<span data-ttu-id="23cc1-115">Obter uma solução de segurança externa específica</span><span class="sxs-lookup"><span data-stu-id="23cc1-115">Get a specific external security solution</span></span>

## <span data-ttu-id="23cc1-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="23cc1-116">PARAMETERS</span></span>

### <span data-ttu-id="23cc1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23cc1-117">-DefaultProfile</span></span>
<span data-ttu-id="23cc1-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="23cc1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23cc1-119">-Local</span><span class="sxs-lookup"><span data-stu-id="23cc1-119">-Location</span></span>
<span data-ttu-id="23cc1-120">Localização.</span><span class="sxs-lookup"><span data-stu-id="23cc1-120">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23cc1-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="23cc1-121">-Name</span></span>
<span data-ttu-id="23cc1-122">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="23cc1-122">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23cc1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23cc1-123">-ResourceGroupName</span></span>
<span data-ttu-id="23cc1-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="23cc1-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23cc1-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="23cc1-125">-ResourceId</span></span>
<span data-ttu-id="23cc1-126">ID do Recurso.</span><span class="sxs-lookup"><span data-stu-id="23cc1-126">Resource ID.</span></span>

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

### <span data-ttu-id="23cc1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23cc1-127">CommonParameters</span></span>
<span data-ttu-id="23cc1-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23cc1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23cc1-129">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="23cc1-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23cc1-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="23cc1-130">INPUTS</span></span>

### <span data-ttu-id="23cc1-131">System.String</span><span class="sxs-lookup"><span data-stu-id="23cc1-131">System.String</span></span>

## <span data-ttu-id="23cc1-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="23cc1-132">OUTPUTS</span></span>

### <span data-ttu-id="23cc1-133">Microsoft.Azure.Commands.Security.Models.ExternalSecuritySolutions.PSSecurityExternalSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="23cc1-133">Microsoft.Azure.Commands.Security.Models.ExternalSecuritySolutions.PSSecurityExternalSecuritySolution</span></span>

## <span data-ttu-id="23cc1-134">Notas</span><span class="sxs-lookup"><span data-stu-id="23cc1-134">NOTES</span></span>

## <span data-ttu-id="23cc1-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="23cc1-135">RELATED LINKS</span></span>
