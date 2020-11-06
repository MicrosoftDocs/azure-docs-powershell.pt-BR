---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotConfigName.md
ms.openlocfilehash: b1b9760d129a4177f979996f1ef46bd2a225f452
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93601950"
---
# <span data-ttu-id="8d97e-101">Get-AzureRmWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="8d97e-101">Get-AzureRmWebAppSlotConfigName</span></span>

## <span data-ttu-id="8d97e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8d97e-102">SYNOPSIS</span></span>
<span data-ttu-id="8d97e-103">Obter a lista de nomes de configuração de slots do aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="8d97e-103">Get the list of Web App Slot Config names</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d97e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8d97e-104">SYNTAX</span></span>

### <span data-ttu-id="8d97e-105">Eles</span><span class="sxs-lookup"><span data-stu-id="8d97e-105">S1</span></span>
```
Get-AzureRmWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d97e-106">S2</span><span class="sxs-lookup"><span data-stu-id="8d97e-106">S2</span></span>
```
Get-AzureRmWebAppSlotConfigName [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8d97e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8d97e-107">DESCRIPTION</span></span>
<span data-ttu-id="8d97e-108">O cmdlet **Get-AzureRmWebAppSlotConfigName** recupera a lista de configurações do aplicativo e nomes de cadeias de conexão que estão marcados atualmente como configurações de slot</span><span class="sxs-lookup"><span data-stu-id="8d97e-108">The **Get-AzureRmWebAppSlotConfigName** cmdlet retrieves the list of App Setting and Connection String names that are currently marked as slot settings</span></span>

## <span data-ttu-id="8d97e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8d97e-109">EXAMPLES</span></span>

### <span data-ttu-id="8d97e-110">1:</span><span class="sxs-lookup"><span data-stu-id="8d97e-110">1:</span></span>
```
PS C:\>Get-AzureRmWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="8d97e-111">Este comando obtém as configurações do aplicativo e cadeias de conexão pertinentes ao aplicativo Web chamado ContosoSite associado ao grupo de recursos padrão-Web-Oesteus</span><span class="sxs-lookup"><span data-stu-id="8d97e-111">This command gets App Settings and Connection strings pertaining to the Web App named ContosoSite associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="8d97e-112">OS</span><span class="sxs-lookup"><span data-stu-id="8d97e-112">PARAMETERS</span></span>

### <span data-ttu-id="8d97e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d97e-113">-DefaultProfile</span></span>
<span data-ttu-id="8d97e-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8d97e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d97e-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="8d97e-115">-Name</span></span>
<span data-ttu-id="8d97e-116">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="8d97e-116">WebApp Name</span></span>

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

### <span data-ttu-id="8d97e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d97e-117">-ResourceGroupName</span></span>
<span data-ttu-id="8d97e-118">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="8d97e-118">Resource Group Name</span></span>

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

### <span data-ttu-id="8d97e-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="8d97e-119">-WebApp</span></span>
<span data-ttu-id="8d97e-120">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="8d97e-120">WebApp Object</span></span>

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

### <span data-ttu-id="8d97e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d97e-121">CommonParameters</span></span>
<span data-ttu-id="8d97e-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d97e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d97e-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d97e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d97e-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8d97e-124">INPUTS</span></span>

### <span data-ttu-id="8d97e-125">System. String</span><span class="sxs-lookup"><span data-stu-id="8d97e-125">System.String</span></span>

### <span data-ttu-id="8d97e-126">Microsoft. Azure. Management. WebSites. Models. site</span><span class="sxs-lookup"><span data-stu-id="8d97e-126">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="8d97e-127">Parâmetros: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8d97e-127">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="8d97e-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8d97e-128">OUTPUTS</span></span>

### <span data-ttu-id="8d97e-129">Microsoft. Azure. Management. WebSites. Models. SlotConfigNamesResource</span><span class="sxs-lookup"><span data-stu-id="8d97e-129">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span></span>

## <span data-ttu-id="8d97e-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8d97e-130">NOTES</span></span>

## <span data-ttu-id="8d97e-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8d97e-131">RELATED LINKS</span></span>
