---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityLocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityLocation.md
ms.openlocfilehash: 77f9283b16aa605da066780165c2fe7b42b1830b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114014"
---
# <span data-ttu-id="adbd4-101">Get-AzSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="adbd4-101">Get-AzSecurityLocation</span></span>

## <span data-ttu-id="adbd4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="adbd4-102">SYNOPSIS</span></span>
<span data-ttu-id="adbd4-103">Obtém o local onde a Central de Segurança do Azure salva automaticamente os dados da assinatura específica</span><span class="sxs-lookup"><span data-stu-id="adbd4-103">Gets the location where Azure Security Center will automatically save data for the specific subscription</span></span>

## <span data-ttu-id="adbd4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="adbd4-104">SYNTAX</span></span>

### <span data-ttu-id="adbd4-105">SubscriptionScope (Padrão)</span><span class="sxs-lookup"><span data-stu-id="adbd4-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityLocation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="adbd4-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="adbd4-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityLocation -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="adbd4-107">Resourceid</span><span class="sxs-lookup"><span data-stu-id="adbd4-107">ResourceId</span></span>
```
Get-AzSecurityLocation -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="adbd4-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="adbd4-108">DESCRIPTION</span></span>
<span data-ttu-id="adbd4-109">A Central de Segurança do Azure decidirá automaticamente sobre um local para salvar alguns dos seus dados.</span><span class="sxs-lookup"><span data-stu-id="adbd4-109">Azure Security Center will automatically decide on a location to save some of your data.</span></span>
<span data-ttu-id="adbd4-110">Use este cmdlet para descobrir esse local.</span><span class="sxs-lookup"><span data-stu-id="adbd4-110">Use this cmdlet to discover that location.</span></span>

## <span data-ttu-id="adbd4-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="adbd4-111">EXAMPLES</span></span>

### <span data-ttu-id="adbd4-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="adbd4-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityLocation
Id                                                                                                   Name
--                                                                                                   ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus centralus
```

<span data-ttu-id="adbd4-113">Obtém o local onde a Central de Segurança do Azure salva os dados de segurança calculados.</span><span class="sxs-lookup"><span data-stu-id="adbd4-113">Gets the location where Azure Security Center saves the calculated security data.</span></span>

## <span data-ttu-id="adbd4-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="adbd4-114">PARAMETERS</span></span>

### <span data-ttu-id="adbd4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adbd4-115">-DefaultProfile</span></span>
<span data-ttu-id="adbd4-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="adbd4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="adbd4-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="adbd4-117">-Name</span></span>
<span data-ttu-id="adbd4-118">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="adbd4-118">Resource name.</span></span>

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

### <span data-ttu-id="adbd4-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="adbd4-119">-ResourceId</span></span>
<span data-ttu-id="adbd4-120">ID do Recurso.</span><span class="sxs-lookup"><span data-stu-id="adbd4-120">Resource ID.</span></span>

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

### <span data-ttu-id="adbd4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adbd4-121">CommonParameters</span></span>
<span data-ttu-id="adbd4-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adbd4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adbd4-123">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="adbd4-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adbd4-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="adbd4-124">INPUTS</span></span>

### <span data-ttu-id="adbd4-125">System.String</span><span class="sxs-lookup"><span data-stu-id="adbd4-125">System.String</span></span>

## <span data-ttu-id="adbd4-126">Saídas</span><span class="sxs-lookup"><span data-stu-id="adbd4-126">OUTPUTS</span></span>

### <span data-ttu-id="adbd4-127">Microsoft.Azure.Commands.Security.Models.Locations.PSSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="adbd4-127">Microsoft.Azure.Commands.Security.Models.Locations.PSSecurityLocation</span></span>

## <span data-ttu-id="adbd4-128">Notas</span><span class="sxs-lookup"><span data-stu-id="adbd4-128">NOTES</span></span>

## <span data-ttu-id="adbd4-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="adbd4-129">RELATED LINKS</span></span>
