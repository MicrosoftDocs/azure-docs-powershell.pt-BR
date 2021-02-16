---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
ms.openlocfilehash: 9ca0578aacbd0ca970211bc38419880cbe99675b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118504"
---
# <span data-ttu-id="ed35b-101">Get-AzWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="ed35b-101">Get-AzWebAppSlotConfigName</span></span>

## <span data-ttu-id="ed35b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ed35b-102">SYNOPSIS</span></span>
<span data-ttu-id="ed35b-103">Obter a lista de nomes de Configuração de Slot do Web App</span><span class="sxs-lookup"><span data-stu-id="ed35b-103">Get the list of Web App Slot Config names</span></span>

## <span data-ttu-id="ed35b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ed35b-104">SYNTAX</span></span>

### <span data-ttu-id="ed35b-105">S1</span><span class="sxs-lookup"><span data-stu-id="ed35b-105">S1</span></span>
```
Get-AzWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed35b-106">S2</span><span class="sxs-lookup"><span data-stu-id="ed35b-106">S2</span></span>
```
Get-AzWebAppSlotConfigName [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed35b-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed35b-107">DESCRIPTION</span></span>
<span data-ttu-id="ed35b-108">O cmdlet **Get-AzWebAppSlotConfigName** recupera a lista de nomes de Cadeia de Conexão e Configuração de Aplicativos marcados como configurações de slot</span><span class="sxs-lookup"><span data-stu-id="ed35b-108">The **Get-AzWebAppSlotConfigName** cmdlet retrieves the list of App Setting and Connection String names that are currently marked as slot settings</span></span>

## <span data-ttu-id="ed35b-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ed35b-109">EXAMPLES</span></span>

### <span data-ttu-id="ed35b-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ed35b-110">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="ed35b-111">Este comando obtém configurações de aplicativo e cadeias de conexão referentes ao Aplicativo Web chamado ContosoSite associado ao grupo de recursos Default-Web-WestUS</span><span class="sxs-lookup"><span data-stu-id="ed35b-111">This command gets App Settings and Connection strings pertaining to the Web App named ContosoSite associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="ed35b-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ed35b-112">PARAMETERS</span></span>

### <span data-ttu-id="ed35b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed35b-113">-DefaultProfile</span></span>
<span data-ttu-id="ed35b-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="ed35b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed35b-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="ed35b-115">-Name</span></span>
<span data-ttu-id="ed35b-116">Nome webapp</span><span class="sxs-lookup"><span data-stu-id="ed35b-116">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed35b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed35b-117">-ResourceGroupName</span></span>
<span data-ttu-id="ed35b-118">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="ed35b-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed35b-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ed35b-119">-WebApp</span></span>
<span data-ttu-id="ed35b-120">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="ed35b-120">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed35b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed35b-121">CommonParameters</span></span>
<span data-ttu-id="ed35b-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed35b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed35b-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed35b-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed35b-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="ed35b-124">INPUTS</span></span>

### <span data-ttu-id="ed35b-125">System.String</span><span class="sxs-lookup"><span data-stu-id="ed35b-125">System.String</span></span>

### <span data-ttu-id="ed35b-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="ed35b-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ed35b-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="ed35b-127">OUTPUTS</span></span>

### <span data-ttu-id="ed35b-128">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span><span class="sxs-lookup"><span data-stu-id="ed35b-128">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span></span>

## <span data-ttu-id="ed35b-129">Notas</span><span class="sxs-lookup"><span data-stu-id="ed35b-129">NOTES</span></span>

## <span data-ttu-id="ed35b-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ed35b-130">RELATED LINKS</span></span>
