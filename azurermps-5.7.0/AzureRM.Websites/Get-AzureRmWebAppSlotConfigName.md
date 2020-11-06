---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotConfigName.md
ms.openlocfilehash: 96e9c5945938addfbd629ef66b5f68e54c0427e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428683"
---
# <span data-ttu-id="69b54-101">Get-AzureRmWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="69b54-101">Get-AzureRmWebAppSlotConfigName</span></span>

## <span data-ttu-id="69b54-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="69b54-102">SYNOPSIS</span></span>
<span data-ttu-id="69b54-103">Obter a lista de nomes de configuração de slots do aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="69b54-103">Get the list of Web App Slot Config names</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69b54-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="69b54-104">SYNTAX</span></span>

### <span data-ttu-id="69b54-105">Eles</span><span class="sxs-lookup"><span data-stu-id="69b54-105">S1</span></span>
```
Get-AzureRmWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69b54-106">S2</span><span class="sxs-lookup"><span data-stu-id="69b54-106">S2</span></span>
```
Get-AzureRmWebAppSlotConfigName [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="69b54-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="69b54-107">DESCRIPTION</span></span>
<span data-ttu-id="69b54-108">O cmdlet **Get-AzureRmWebAppSlotConfigName** recupera a lista de configurações do aplicativo e nomes de cadeias de conexão que estão marcados atualmente como configurações de slot</span><span class="sxs-lookup"><span data-stu-id="69b54-108">The **Get-AzureRmWebAppSlotConfigName** cmdlet retrieves the list of App Setting and Connection String names that are currently marked as slot settings</span></span>

## <span data-ttu-id="69b54-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="69b54-109">EXAMPLES</span></span>

### <span data-ttu-id="69b54-110">1:</span><span class="sxs-lookup"><span data-stu-id="69b54-110">1:</span></span>
```
PS C:\>Get-AzureRmWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="69b54-111">Este comando obtém as configurações do aplicativo e cadeias de conexão pertinentes ao aplicativo Web chamado ContosoSite associado ao grupo de recursos padrão-Web-Oesteus</span><span class="sxs-lookup"><span data-stu-id="69b54-111">This command gets App Settings and Connection strings pertaining to the Web App named ContosoSite associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="69b54-112">OS</span><span class="sxs-lookup"><span data-stu-id="69b54-112">PARAMETERS</span></span>

### <span data-ttu-id="69b54-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69b54-113">-DefaultProfile</span></span>
<span data-ttu-id="69b54-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="69b54-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69b54-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="69b54-115">-Name</span></span>
<span data-ttu-id="69b54-116">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="69b54-116">WebApp Name</span></span>

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

### <span data-ttu-id="69b54-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69b54-117">-ResourceGroupName</span></span>
<span data-ttu-id="69b54-118">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="69b54-118">Resource Group Name</span></span>

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

### <span data-ttu-id="69b54-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="69b54-119">-WebApp</span></span>
<span data-ttu-id="69b54-120">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="69b54-120">WebApp Object</span></span>

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

### <span data-ttu-id="69b54-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69b54-121">CommonParameters</span></span>
<span data-ttu-id="69b54-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69b54-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69b54-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69b54-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69b54-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="69b54-124">INPUTS</span></span>

### <span data-ttu-id="69b54-125">Instalação</span><span class="sxs-lookup"><span data-stu-id="69b54-125">Site</span></span>
<span data-ttu-id="69b54-126">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="69b54-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="69b54-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="69b54-127">OUTPUTS</span></span>

## <span data-ttu-id="69b54-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="69b54-128">NOTES</span></span>

## <span data-ttu-id="69b54-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="69b54-129">RELATED LINKS</span></span>

