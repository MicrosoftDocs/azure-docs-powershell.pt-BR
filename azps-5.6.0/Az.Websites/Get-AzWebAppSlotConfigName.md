---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
ms.openlocfilehash: 2157c7a570f38838a65e1d4bba40dade22e10367
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886707"
---
# <span data-ttu-id="72708-101">Get-AzWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="72708-101">Get-AzWebAppSlotConfigName</span></span>

## <span data-ttu-id="72708-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72708-102">SYNOPSIS</span></span>
<span data-ttu-id="72708-103">Obter a lista de nomes de Configuração de Slot de Aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="72708-103">Get the list of Web App Slot Config names</span></span>

## <span data-ttu-id="72708-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="72708-104">SYNTAX</span></span>

### <span data-ttu-id="72708-105">S1</span><span class="sxs-lookup"><span data-stu-id="72708-105">S1</span></span>
```
Get-AzWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72708-106">S2</span><span class="sxs-lookup"><span data-stu-id="72708-106">S2</span></span>
```
Get-AzWebAppSlotConfigName [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72708-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="72708-107">DESCRIPTION</span></span>
<span data-ttu-id="72708-108">O cmdlet **Get-AzWebAppSlotConfigName** recupera a lista de nomes de Cadeia de Caracteres de Conexão e Configuração de Aplicativo que estão marcados atualmente como configurações de slot</span><span class="sxs-lookup"><span data-stu-id="72708-108">The **Get-AzWebAppSlotConfigName** cmdlet retrieves the list of App Setting and Connection String names that are currently marked as slot settings</span></span>

## <span data-ttu-id="72708-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="72708-109">EXAMPLES</span></span>

### <span data-ttu-id="72708-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="72708-110">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="72708-111">Este comando obtém configurações de aplicativo e cadeias de caracteres de conexão pertencentes ao Aplicativo Web chamado ContosoSite associado ao grupo de recursos Default-Web-WestUS</span><span class="sxs-lookup"><span data-stu-id="72708-111">This command gets App Settings and Connection strings pertaining to the Web App named ContosoSite associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="72708-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="72708-112">PARAMETERS</span></span>

### <span data-ttu-id="72708-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72708-113">-DefaultProfile</span></span>
<span data-ttu-id="72708-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="72708-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72708-115">-Name</span><span class="sxs-lookup"><span data-stu-id="72708-115">-Name</span></span>
<span data-ttu-id="72708-116">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="72708-116">WebApp Name</span></span>

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

### <span data-ttu-id="72708-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72708-117">-ResourceGroupName</span></span>
<span data-ttu-id="72708-118">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="72708-118">Resource Group Name</span></span>

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

### <span data-ttu-id="72708-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="72708-119">-WebApp</span></span>
<span data-ttu-id="72708-120">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="72708-120">WebApp Object</span></span>

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

### <span data-ttu-id="72708-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72708-121">CommonParameters</span></span>
<span data-ttu-id="72708-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72708-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72708-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72708-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72708-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="72708-124">INPUTS</span></span>

### <span data-ttu-id="72708-125">System.String</span><span class="sxs-lookup"><span data-stu-id="72708-125">System.String</span></span>

### <span data-ttu-id="72708-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="72708-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="72708-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="72708-127">OUTPUTS</span></span>

### <span data-ttu-id="72708-128">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span><span class="sxs-lookup"><span data-stu-id="72708-128">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span></span>

## <span data-ttu-id="72708-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="72708-129">NOTES</span></span>

## <span data-ttu-id="72708-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="72708-130">RELATED LINKS</span></span>
