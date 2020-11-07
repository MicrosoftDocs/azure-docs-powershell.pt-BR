---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityLocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityLocation.md
ms.openlocfilehash: 2de4a80f2770624bb520aa4236a5d92bea97fdf0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773267"
---
# <span data-ttu-id="66688-101">Get-AzSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="66688-101">Get-AzSecurityLocation</span></span>

## <span data-ttu-id="66688-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="66688-102">SYNOPSIS</span></span>
<span data-ttu-id="66688-103">Obtém o local onde a central de segurança do Azure salvará automaticamente os dados para a assinatura específica</span><span class="sxs-lookup"><span data-stu-id="66688-103">Gets the location where Azure Security Center will automatically save data for the specific subscription</span></span>

## <span data-ttu-id="66688-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="66688-104">SYNTAX</span></span>

### <span data-ttu-id="66688-105">SubscriptionScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="66688-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityLocation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66688-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="66688-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityLocation -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66688-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="66688-107">ResourceId</span></span>
```
Get-AzSecurityLocation -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66688-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="66688-108">DESCRIPTION</span></span>
<span data-ttu-id="66688-109">A central de segurança do Azure decidirá automaticamente um local para salvar alguns dos seus dados.</span><span class="sxs-lookup"><span data-stu-id="66688-109">Azure Security Center will automatically decide on a location to save some of your data.</span></span>
<span data-ttu-id="66688-110">Use esse cmdlet para descobrir esse local.</span><span class="sxs-lookup"><span data-stu-id="66688-110">Use this cmdlet to discover that location.</span></span>

## <span data-ttu-id="66688-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="66688-111">EXAMPLES</span></span>

### <span data-ttu-id="66688-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="66688-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityLocation
Id                                                                                                   Name
--                                                                                                   ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus centralus
```

<span data-ttu-id="66688-113">Obtém o local onde a central de segurança do Azure salva os dados de segurança calculados.</span><span class="sxs-lookup"><span data-stu-id="66688-113">Gets the location where Azure Security Center saves the calculated security data.</span></span>

## <span data-ttu-id="66688-114">OS</span><span class="sxs-lookup"><span data-stu-id="66688-114">PARAMETERS</span></span>

### <span data-ttu-id="66688-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66688-115">-DefaultProfile</span></span>
<span data-ttu-id="66688-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="66688-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66688-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="66688-117">-Name</span></span>
<span data-ttu-id="66688-118">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="66688-118">Resource name.</span></span>

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

### <span data-ttu-id="66688-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="66688-119">-ResourceId</span></span>
<span data-ttu-id="66688-120">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="66688-120">Resource ID.</span></span>

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

### <span data-ttu-id="66688-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66688-121">CommonParameters</span></span>
<span data-ttu-id="66688-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66688-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66688-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66688-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66688-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="66688-124">INPUTS</span></span>

### <span data-ttu-id="66688-125">System. String</span><span class="sxs-lookup"><span data-stu-id="66688-125">System.String</span></span>

## <span data-ttu-id="66688-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="66688-126">OUTPUTS</span></span>

### <span data-ttu-id="66688-127">Microsoft. Azure. Commands. Security. Models. Locations. PSSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="66688-127">Microsoft.Azure.Commands.Security.Models.Locations.PSSecurityLocation</span></span>

## <span data-ttu-id="66688-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="66688-128">NOTES</span></span>

## <span data-ttu-id="66688-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="66688-129">RELATED LINKS</span></span>
