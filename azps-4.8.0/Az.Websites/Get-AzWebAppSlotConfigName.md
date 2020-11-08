---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
ms.openlocfilehash: 9ca0578aacbd0ca970211bc38419880cbe99675b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110704"
---
# <span data-ttu-id="e44bb-101">Get-AzWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="e44bb-101">Get-AzWebAppSlotConfigName</span></span>

## <span data-ttu-id="e44bb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e44bb-102">SYNOPSIS</span></span>
<span data-ttu-id="e44bb-103">Obter a lista de nomes de configuração de slots do aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="e44bb-103">Get the list of Web App Slot Config names</span></span>

## <span data-ttu-id="e44bb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e44bb-104">SYNTAX</span></span>

### <span data-ttu-id="e44bb-105">Eles</span><span class="sxs-lookup"><span data-stu-id="e44bb-105">S1</span></span>
```
Get-AzWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e44bb-106">S2</span><span class="sxs-lookup"><span data-stu-id="e44bb-106">S2</span></span>
```
Get-AzWebAppSlotConfigName [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e44bb-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e44bb-107">DESCRIPTION</span></span>
<span data-ttu-id="e44bb-108">O cmdlet **Get-AzWebAppSlotConfigName** recupera a lista de configurações do aplicativo e nomes de cadeias de conexão que estão marcados atualmente como configurações de slot</span><span class="sxs-lookup"><span data-stu-id="e44bb-108">The **Get-AzWebAppSlotConfigName** cmdlet retrieves the list of App Setting and Connection String names that are currently marked as slot settings</span></span>

## <span data-ttu-id="e44bb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e44bb-109">EXAMPLES</span></span>

### <span data-ttu-id="e44bb-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e44bb-110">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="e44bb-111">Este comando obtém as configurações do aplicativo e cadeias de conexão pertinentes ao aplicativo Web chamado ContosoSite associado ao grupo de recursos padrão-Web-Oesteus</span><span class="sxs-lookup"><span data-stu-id="e44bb-111">This command gets App Settings and Connection strings pertaining to the Web App named ContosoSite associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="e44bb-112">OS</span><span class="sxs-lookup"><span data-stu-id="e44bb-112">PARAMETERS</span></span>

### <span data-ttu-id="e44bb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e44bb-113">-DefaultProfile</span></span>
<span data-ttu-id="e44bb-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e44bb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e44bb-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="e44bb-115">-Name</span></span>
<span data-ttu-id="e44bb-116">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="e44bb-116">WebApp Name</span></span>

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

### <span data-ttu-id="e44bb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e44bb-117">-ResourceGroupName</span></span>
<span data-ttu-id="e44bb-118">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="e44bb-118">Resource Group Name</span></span>

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

### <span data-ttu-id="e44bb-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="e44bb-119">-WebApp</span></span>
<span data-ttu-id="e44bb-120">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="e44bb-120">WebApp Object</span></span>

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

### <span data-ttu-id="e44bb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e44bb-121">CommonParameters</span></span>
<span data-ttu-id="e44bb-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e44bb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e44bb-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e44bb-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e44bb-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e44bb-124">INPUTS</span></span>

### <span data-ttu-id="e44bb-125">System. String</span><span class="sxs-lookup"><span data-stu-id="e44bb-125">System.String</span></span>

### <span data-ttu-id="e44bb-126">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="e44bb-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="e44bb-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e44bb-127">OUTPUTS</span></span>

### <span data-ttu-id="e44bb-128">Microsoft. Azure. Management. WebSites. Models. SlotConfigNamesResource</span><span class="sxs-lookup"><span data-stu-id="e44bb-128">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span></span>

## <span data-ttu-id="e44bb-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e44bb-129">NOTES</span></span>

## <span data-ttu-id="e44bb-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e44bb-130">RELATED LINKS</span></span>
