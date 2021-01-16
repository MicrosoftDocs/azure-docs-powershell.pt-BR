---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppTrafficRouting.md
ms.openlocfilehash: fb8d23ad24f8e9ab0b6e951d39ba7445d336176f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263641"
---
# <span data-ttu-id="acc79-101">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="acc79-101">Get-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="acc79-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="acc79-102">SYNOPSIS</span></span>
<span data-ttu-id="acc79-103">Obtenha uma regra de roteamento para o nome do slot fornecido.</span><span class="sxs-lookup"><span data-stu-id="acc79-103">Get a routing Rule for the given Slot name.</span></span>

## <span data-ttu-id="acc79-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="acc79-104">SYNTAX</span></span>

```
Get-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RuleName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="acc79-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="acc79-105">DESCRIPTION</span></span>
<span data-ttu-id="acc79-106">O cmdlet **Get-AzWebAppTrafficRouting** Obtém uma configuração de regra de roteamento de um slot do aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="acc79-106">The **Get-AzWebAppTrafficRouting** cmdlet Gets a routing rule configuration from an Azure Web App Slot.</span></span>

## <span data-ttu-id="acc79-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="acc79-107">EXAMPLES</span></span>

### <span data-ttu-id="acc79-108">O exemplo 1 Obtém a regra de roteamento específica do slot webapp</span><span class="sxs-lookup"><span data-stu-id="acc79-108">Example 1 Gets the specific routing rule from webapp slot</span></span>
```powershell
PS C:\> Get-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite"  -RuleName 'Stg'
```

<span data-ttu-id="acc79-109">Esse comando obtém uma regra de roteamento para um determinado slot do webapp.</span><span class="sxs-lookup"><span data-stu-id="acc79-109">This command gets a routing rule for a given webapp slot.</span></span>

## <span data-ttu-id="acc79-110">OS</span><span class="sxs-lookup"><span data-stu-id="acc79-110">PARAMETERS</span></span>

### <span data-ttu-id="acc79-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acc79-111">-DefaultProfile</span></span>
<span data-ttu-id="acc79-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="acc79-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="acc79-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acc79-113">-ResourceGroupName</span></span>
<span data-ttu-id="acc79-114">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="acc79-114">Resource Group Name</span></span>

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

### <span data-ttu-id="acc79-115">-RuleName</span><span class="sxs-lookup"><span data-stu-id="acc79-115">-RuleName</span></span>
<span data-ttu-id="acc79-116">Nome da regra</span><span class="sxs-lookup"><span data-stu-id="acc79-116">Rule Name</span></span>
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

### <span data-ttu-id="acc79-117">-WebAppname</span><span class="sxs-lookup"><span data-stu-id="acc79-117">-WebAppName</span></span>
<span data-ttu-id="acc79-118">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="acc79-118">WebApp Name</span></span>

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

### <span data-ttu-id="acc79-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acc79-119">CommonParameters</span></span>
<span data-ttu-id="acc79-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acc79-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acc79-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="acc79-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acc79-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="acc79-122">INPUTS</span></span>

### <span data-ttu-id="acc79-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="acc79-123">None</span></span>

## <span data-ttu-id="acc79-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="acc79-124">OUTPUTS</span></span>

### <span data-ttu-id="acc79-125">Microsoft. Azure. Management. WebSites. Models. RampUpRule</span><span class="sxs-lookup"><span data-stu-id="acc79-125">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="acc79-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="acc79-126">NOTES</span></span>

## <span data-ttu-id="acc79-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="acc79-127">RELATED LINKS</span></span>

[<span data-ttu-id="acc79-128">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="acc79-128">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)

[<span data-ttu-id="acc79-129">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="acc79-129">Add-AzWebAppTrafficRouting</span></span>](./Add-AzWebAppTrafficRouting.md)

[<span data-ttu-id="acc79-130">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="acc79-130">Remove-AzWebAppTrafficRouting</span></span>](./Remove-AzWebAppTrafficRouting.md)
