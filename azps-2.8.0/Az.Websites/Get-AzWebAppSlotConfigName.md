---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
ms.openlocfilehash: bd871e75e5a4f9c8e5c28e8788c8ef291a88e6db
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774414"
---
# <span data-ttu-id="d7da0-101">Get-AzWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="d7da0-101">Get-AzWebAppSlotConfigName</span></span>

## <span data-ttu-id="d7da0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d7da0-102">SYNOPSIS</span></span>
<span data-ttu-id="d7da0-103">Obter a lista de nomes de configuração de slots do aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="d7da0-103">Get the list of Web App Slot Config names</span></span>

## <span data-ttu-id="d7da0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d7da0-104">SYNTAX</span></span>

### <span data-ttu-id="d7da0-105">Eles</span><span class="sxs-lookup"><span data-stu-id="d7da0-105">S1</span></span>
```
Get-AzWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7da0-106">S2</span><span class="sxs-lookup"><span data-stu-id="d7da0-106">S2</span></span>
```
Get-AzWebAppSlotConfigName [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7da0-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d7da0-107">DESCRIPTION</span></span>
<span data-ttu-id="d7da0-108">O cmdlet **Get-AzWebAppSlotConfigName** recupera a lista de configurações do aplicativo e nomes de cadeias de conexão que estão marcados atualmente como configurações de slot</span><span class="sxs-lookup"><span data-stu-id="d7da0-108">The **Get-AzWebAppSlotConfigName** cmdlet retrieves the list of App Setting and Connection String names that are currently marked as slot settings</span></span>

## <span data-ttu-id="d7da0-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d7da0-109">EXAMPLES</span></span>

### <span data-ttu-id="d7da0-110">1:</span><span class="sxs-lookup"><span data-stu-id="d7da0-110">1:</span></span>
```
PS C:\>Get-AzWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="d7da0-111">Este comando obtém as configurações do aplicativo e cadeias de conexão pertinentes ao aplicativo Web chamado ContosoSite associado ao grupo de recursos padrão-Web-Oesteus</span><span class="sxs-lookup"><span data-stu-id="d7da0-111">This command gets App Settings and Connection strings pertaining to the Web App named ContosoSite associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="d7da0-112">OS</span><span class="sxs-lookup"><span data-stu-id="d7da0-112">PARAMETERS</span></span>

### <span data-ttu-id="d7da0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7da0-113">-DefaultProfile</span></span>
<span data-ttu-id="d7da0-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d7da0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7da0-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="d7da0-115">-Name</span></span>
<span data-ttu-id="d7da0-116">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="d7da0-116">WebApp Name</span></span>

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

### <span data-ttu-id="d7da0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7da0-117">-ResourceGroupName</span></span>
<span data-ttu-id="d7da0-118">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="d7da0-118">Resource Group Name</span></span>

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

### <span data-ttu-id="d7da0-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="d7da0-119">-WebApp</span></span>
<span data-ttu-id="d7da0-120">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="d7da0-120">WebApp Object</span></span>

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

### <span data-ttu-id="d7da0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7da0-121">CommonParameters</span></span>
<span data-ttu-id="d7da0-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7da0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7da0-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7da0-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7da0-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d7da0-124">INPUTS</span></span>

### <span data-ttu-id="d7da0-125">System. String</span><span class="sxs-lookup"><span data-stu-id="d7da0-125">System.String</span></span>

### <span data-ttu-id="d7da0-126">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="d7da0-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="d7da0-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d7da0-127">OUTPUTS</span></span>

### <span data-ttu-id="d7da0-128">Microsoft. Azure. Management. WebSites. Models. SlotConfigNamesResource</span><span class="sxs-lookup"><span data-stu-id="d7da0-128">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span></span>

## <span data-ttu-id="d7da0-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d7da0-129">NOTES</span></span>

## <span data-ttu-id="d7da0-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d7da0-130">RELATED LINKS</span></span>
