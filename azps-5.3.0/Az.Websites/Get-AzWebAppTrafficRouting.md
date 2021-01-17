---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppTrafficRouting.md
ms.openlocfilehash: fb8d23ad24f8e9ab0b6e951d39ba7445d336176f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427819"
---
# <span data-ttu-id="b4693-101">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="b4693-101">Get-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="b4693-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b4693-102">SYNOPSIS</span></span>
<span data-ttu-id="b4693-103">Obtenha uma regra de roteamento para o nome do slot fornecido.</span><span class="sxs-lookup"><span data-stu-id="b4693-103">Get a routing Rule for the given Slot name.</span></span>

## <span data-ttu-id="b4693-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b4693-104">SYNTAX</span></span>

```
Get-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RuleName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4693-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b4693-105">DESCRIPTION</span></span>
<span data-ttu-id="b4693-106">O cmdlet **Get-AzWebAppTrafficRouting** Obtém uma configuração de regra de roteamento de um slot do aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="b4693-106">The **Get-AzWebAppTrafficRouting** cmdlet Gets a routing rule configuration from an Azure Web App Slot.</span></span>

## <span data-ttu-id="b4693-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b4693-107">EXAMPLES</span></span>

### <span data-ttu-id="b4693-108">O exemplo 1 Obtém a regra de roteamento específica do slot webapp</span><span class="sxs-lookup"><span data-stu-id="b4693-108">Example 1 Gets the specific routing rule from webapp slot</span></span>
```powershell
PS C:\> Get-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite"  -RuleName 'Stg'
```

<span data-ttu-id="b4693-109">Esse comando obtém uma regra de roteamento para um determinado slot do webapp.</span><span class="sxs-lookup"><span data-stu-id="b4693-109">This command gets a routing rule for a given webapp slot.</span></span>

## <span data-ttu-id="b4693-110">OS</span><span class="sxs-lookup"><span data-stu-id="b4693-110">PARAMETERS</span></span>

### <span data-ttu-id="b4693-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4693-111">-DefaultProfile</span></span>
<span data-ttu-id="b4693-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b4693-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4693-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4693-113">-ResourceGroupName</span></span>
<span data-ttu-id="b4693-114">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="b4693-114">Resource Group Name</span></span>

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

### <span data-ttu-id="b4693-115">-RuleName</span><span class="sxs-lookup"><span data-stu-id="b4693-115">-RuleName</span></span>
<span data-ttu-id="b4693-116">Nome da regra</span><span class="sxs-lookup"><span data-stu-id="b4693-116">Rule Name</span></span>
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

### <span data-ttu-id="b4693-117">-WebAppname</span><span class="sxs-lookup"><span data-stu-id="b4693-117">-WebAppName</span></span>
<span data-ttu-id="b4693-118">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="b4693-118">WebApp Name</span></span>

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

### <span data-ttu-id="b4693-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4693-119">CommonParameters</span></span>
<span data-ttu-id="b4693-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4693-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4693-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4693-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4693-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b4693-122">INPUTS</span></span>

### <span data-ttu-id="b4693-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="b4693-123">None</span></span>

## <span data-ttu-id="b4693-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b4693-124">OUTPUTS</span></span>

### <span data-ttu-id="b4693-125">Microsoft. Azure. Management. WebSites. Models. RampUpRule</span><span class="sxs-lookup"><span data-stu-id="b4693-125">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="b4693-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b4693-126">NOTES</span></span>

## <span data-ttu-id="b4693-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b4693-127">RELATED LINKS</span></span>

[<span data-ttu-id="b4693-128">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="b4693-128">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)

[<span data-ttu-id="b4693-129">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="b4693-129">Add-AzWebAppTrafficRouting</span></span>](./Add-AzWebAppTrafficRouting.md)

[<span data-ttu-id="b4693-130">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="b4693-130">Remove-AzWebAppTrafficRouting</span></span>](./Remove-AzWebAppTrafficRouting.md)
