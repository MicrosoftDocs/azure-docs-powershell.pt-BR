---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslotconfigname
schema: 2.0.0
ms.openlocfilehash: ff05a30c495475b63b0385f3398c78e0b018a4bc
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786046"
---
# <span data-ttu-id="31ff9-101">Get-AzureRmWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="31ff9-101">Get-AzureRmWebAppSlotConfigName</span></span>

## <span data-ttu-id="31ff9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="31ff9-102">SYNOPSIS</span></span>
<span data-ttu-id="31ff9-103">Obter a lista de nomes de configuração de slots do aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="31ff9-103">Get the list of Web App Slot Config names</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31ff9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="31ff9-104">SYNTAX</span></span>

### <span data-ttu-id="31ff9-105">Eles</span><span class="sxs-lookup"><span data-stu-id="31ff9-105">S1</span></span>
```
Get-AzureRmWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31ff9-106">S2</span><span class="sxs-lookup"><span data-stu-id="31ff9-106">S2</span></span>
```
Get-AzureRmWebAppSlotConfigName [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="31ff9-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="31ff9-107">DESCRIPTION</span></span>
<span data-ttu-id="31ff9-108">O cmdlet **Get-AzureRmWebAppSlotConfigName** recupera a lista de configurações do aplicativo e nomes de cadeias de conexão que estão marcados atualmente como configurações de slot</span><span class="sxs-lookup"><span data-stu-id="31ff9-108">The **Get-AzureRmWebAppSlotConfigName** cmdlet retrieves the list of App Setting and Connection String names that are currently marked as slot settings</span></span>

## <span data-ttu-id="31ff9-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="31ff9-109">EXAMPLES</span></span>

### <span data-ttu-id="31ff9-110">1:</span><span class="sxs-lookup"><span data-stu-id="31ff9-110">1:</span></span>
```
PS C:\>Get-AzureRmWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="31ff9-111">Este comando obtém as configurações do aplicativo e cadeias de conexão pertinentes ao aplicativo Web chamado ContosoSite associado ao grupo de recursos padrão-Web-Oesteus</span><span class="sxs-lookup"><span data-stu-id="31ff9-111">This command gets App Settings and Connection strings pertaining to the Web App named ContosoSite associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="31ff9-112">OS</span><span class="sxs-lookup"><span data-stu-id="31ff9-112">PARAMETERS</span></span>

### <span data-ttu-id="31ff9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31ff9-113">-DefaultProfile</span></span>
<span data-ttu-id="31ff9-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="31ff9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31ff9-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="31ff9-115">-Name</span></span>
<span data-ttu-id="31ff9-116">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="31ff9-116">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31ff9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31ff9-117">-ResourceGroupName</span></span>
<span data-ttu-id="31ff9-118">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="31ff9-118">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31ff9-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="31ff9-119">-WebApp</span></span>
<span data-ttu-id="31ff9-120">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="31ff9-120">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31ff9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31ff9-121">CommonParameters</span></span>
<span data-ttu-id="31ff9-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31ff9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31ff9-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31ff9-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31ff9-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="31ff9-124">INPUTS</span></span>

### <span data-ttu-id="31ff9-125">Instalação</span><span class="sxs-lookup"><span data-stu-id="31ff9-125">Site</span></span>
<span data-ttu-id="31ff9-126">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="31ff9-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="31ff9-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="31ff9-127">OUTPUTS</span></span>

## <span data-ttu-id="31ff9-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="31ff9-128">NOTES</span></span>

## <span data-ttu-id="31ff9-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="31ff9-129">RELATED LINKS</span></span>

