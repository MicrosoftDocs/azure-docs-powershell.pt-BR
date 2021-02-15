---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppTrafficRouting.md
ms.openlocfilehash: fb8d23ad24f8e9ab0b6e951d39ba7445d336176f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116267"
---
# <span data-ttu-id="53612-101">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="53612-101">Get-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="53612-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="53612-102">SYNOPSIS</span></span>
<span data-ttu-id="53612-103">Obter uma Regra de roteamento para o nome de Slot determinado.</span><span class="sxs-lookup"><span data-stu-id="53612-103">Get a routing Rule for the given Slot name.</span></span>

## <span data-ttu-id="53612-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="53612-104">SYNTAX</span></span>

```
Get-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RuleName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53612-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="53612-105">DESCRIPTION</span></span>
<span data-ttu-id="53612-106">O cmdlet **Get-AzWebAppTrafficRouting** obtém uma configuração de regra de roteamento de um Slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="53612-106">The **Get-AzWebAppTrafficRouting** cmdlet Gets a routing rule configuration from an Azure Web App Slot.</span></span>

## <span data-ttu-id="53612-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="53612-107">EXAMPLES</span></span>

### <span data-ttu-id="53612-108">Exemplo 1 Obtém a regra de roteamento específica do slot webapp</span><span class="sxs-lookup"><span data-stu-id="53612-108">Example 1 Gets the specific routing rule from webapp slot</span></span>
```powershell
PS C:\> Get-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite"  -RuleName 'Stg'
```

<span data-ttu-id="53612-109">Esse comando obtém uma regra de roteamento para um determinado slot de webapp.</span><span class="sxs-lookup"><span data-stu-id="53612-109">This command gets a routing rule for a given webapp slot.</span></span>

## <span data-ttu-id="53612-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="53612-110">PARAMETERS</span></span>

### <span data-ttu-id="53612-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53612-111">-DefaultProfile</span></span>
<span data-ttu-id="53612-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="53612-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53612-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53612-113">-ResourceGroupName</span></span>
<span data-ttu-id="53612-114">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="53612-114">Resource Group Name</span></span>

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

### <span data-ttu-id="53612-115">-NomeDa Regra</span><span class="sxs-lookup"><span data-stu-id="53612-115">-RuleName</span></span>
<span data-ttu-id="53612-116">Nome da Regra</span><span class="sxs-lookup"><span data-stu-id="53612-116">Rule Name</span></span>
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

### <span data-ttu-id="53612-117">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="53612-117">-WebAppName</span></span>
<span data-ttu-id="53612-118">Nome webapp</span><span class="sxs-lookup"><span data-stu-id="53612-118">WebApp Name</span></span>

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

### <span data-ttu-id="53612-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53612-119">CommonParameters</span></span>
<span data-ttu-id="53612-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53612-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53612-121">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="53612-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53612-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="53612-122">INPUTS</span></span>

### <span data-ttu-id="53612-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="53612-123">None</span></span>

## <span data-ttu-id="53612-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="53612-124">OUTPUTS</span></span>

### <span data-ttu-id="53612-125">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span><span class="sxs-lookup"><span data-stu-id="53612-125">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="53612-126">Notas</span><span class="sxs-lookup"><span data-stu-id="53612-126">NOTES</span></span>

## <span data-ttu-id="53612-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="53612-127">RELATED LINKS</span></span>

[<span data-ttu-id="53612-128">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="53612-128">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)

[<span data-ttu-id="53612-129">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="53612-129">Add-AzWebAppTrafficRouting</span></span>](./Add-AzWebAppTrafficRouting.md)

[<span data-ttu-id="53612-130">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="53612-130">Remove-AzWebAppTrafficRouting</span></span>](./Remove-AzWebAppTrafficRouting.md)
