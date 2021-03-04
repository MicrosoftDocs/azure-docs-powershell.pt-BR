---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppTrafficRouting.md
ms.openlocfilehash: fb8d23ad24f8e9ab0b6e951d39ba7445d336176f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892580"
---
# <span data-ttu-id="03fa4-101">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="03fa4-101">Get-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="03fa4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03fa4-102">SYNOPSIS</span></span>
<span data-ttu-id="03fa4-103">Obter uma regra de roteamento para o nome slot determinado.</span><span class="sxs-lookup"><span data-stu-id="03fa4-103">Get a routing Rule for the given Slot name.</span></span>

## <span data-ttu-id="03fa4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="03fa4-104">SYNTAX</span></span>

```
Get-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RuleName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03fa4-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="03fa4-105">DESCRIPTION</span></span>
<span data-ttu-id="03fa4-106">O cmdlet **Get-AzWebAppTrafficRouting** obtém uma configuração de regra de roteamento de um Slot do Aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="03fa4-106">The **Get-AzWebAppTrafficRouting** cmdlet Gets a routing rule configuration from an Azure Web App Slot.</span></span>

## <span data-ttu-id="03fa4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="03fa4-107">EXAMPLES</span></span>

### <span data-ttu-id="03fa4-108">Exemplo 1 Obtém a regra de roteamento específica do slot webapp</span><span class="sxs-lookup"><span data-stu-id="03fa4-108">Example 1 Gets the specific routing rule from webapp slot</span></span>
```powershell
PS C:\> Get-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite"  -RuleName 'Stg'
```

<span data-ttu-id="03fa4-109">Este comando obtém uma regra de roteamento para um determinado slot de webapp.</span><span class="sxs-lookup"><span data-stu-id="03fa4-109">This command gets a routing rule for a given webapp slot.</span></span>

## <span data-ttu-id="03fa4-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="03fa4-110">PARAMETERS</span></span>

### <span data-ttu-id="03fa4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03fa4-111">-DefaultProfile</span></span>
<span data-ttu-id="03fa4-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="03fa4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03fa4-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03fa4-113">-ResourceGroupName</span></span>
<span data-ttu-id="03fa4-114">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="03fa4-114">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03fa4-115">-RuleName</span><span class="sxs-lookup"><span data-stu-id="03fa4-115">-RuleName</span></span>
<span data-ttu-id="03fa4-116">Nome da regra</span><span class="sxs-lookup"><span data-stu-id="03fa4-116">Rule Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03fa4-117">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="03fa4-117">-WebAppName</span></span>
<span data-ttu-id="03fa4-118">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="03fa4-118">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03fa4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03fa4-119">CommonParameters</span></span>
<span data-ttu-id="03fa4-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03fa4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03fa4-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="03fa4-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03fa4-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="03fa4-122">INPUTS</span></span>

### <span data-ttu-id="03fa4-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="03fa4-123">None</span></span>

## <span data-ttu-id="03fa4-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="03fa4-124">OUTPUTS</span></span>

### <span data-ttu-id="03fa4-125">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span><span class="sxs-lookup"><span data-stu-id="03fa4-125">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="03fa4-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="03fa4-126">NOTES</span></span>

## <span data-ttu-id="03fa4-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="03fa4-127">RELATED LINKS</span></span>

[<span data-ttu-id="03fa4-128">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="03fa4-128">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)

[<span data-ttu-id="03fa4-129">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="03fa4-129">Add-AzWebAppTrafficRouting</span></span>](./Add-AzWebAppTrafficRouting.md)

[<span data-ttu-id="03fa4-130">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="03fa4-130">Remove-AzWebAppTrafficRouting</span></span>](./Remove-AzWebAppTrafficRouting.md)
