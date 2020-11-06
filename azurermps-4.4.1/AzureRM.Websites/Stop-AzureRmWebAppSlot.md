---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 86E0D477-DD32-49BD-82E7-1CF191E4F612
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebAppSlot.md
ms.openlocfilehash: 91a8c53bc8600006a3a57a5dfefb1141652ca3d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426859"
---
# <span data-ttu-id="4b169-101">Stop-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4b169-101">Stop-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="4b169-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4b169-102">SYNOPSIS</span></span>
<span data-ttu-id="4b169-103">Interrompe um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="4b169-103">Stops an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b169-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4b169-104">SYNTAX</span></span>

### <span data-ttu-id="4b169-105">Eles</span><span class="sxs-lookup"><span data-stu-id="4b169-105">S1</span></span>
```
Stop-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b169-106">S2</span><span class="sxs-lookup"><span data-stu-id="4b169-106">S2</span></span>
```
Stop-AzureRmWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b169-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4b169-107">DESCRIPTION</span></span>
<span data-ttu-id="4b169-108">O cmdlet **Stop-AzureRmWebAppSlot** interrompe um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="4b169-108">The **Stop-AzureRmWebAppSlot** cmdlet stops an Azure Web App Slot.</span></span>

## <span data-ttu-id="4b169-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4b169-109">EXAMPLES</span></span>

### <span data-ttu-id="4b169-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4b169-110">Example 1</span></span>
```
PS C:\>Stop-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="4b169-111">Esse comando interrompe o slot Slot001 pertencente ao aplicativo Web chamado ContosoWebApp que pertence ao grupo de recursos chamado Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="4b169-111">This command stops the slot Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="4b169-112">OS</span><span class="sxs-lookup"><span data-stu-id="4b169-112">PARAMETERS</span></span>

### <span data-ttu-id="4b169-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="4b169-113">-Name</span></span>
<span data-ttu-id="4b169-114">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="4b169-114">WebApp Name</span></span>

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

### <span data-ttu-id="4b169-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b169-115">-ResourceGroupName</span></span>
<span data-ttu-id="4b169-116">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="4b169-116">Resource Group Name</span></span>

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

### <span data-ttu-id="4b169-117">-Slot</span><span class="sxs-lookup"><span data-stu-id="4b169-117">-Slot</span></span>
<span data-ttu-id="4b169-118">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="4b169-118">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b169-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="4b169-119">-WebApp</span></span>
<span data-ttu-id="4b169-120">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="4b169-120">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4b169-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b169-121">-DefaultProfile</span></span>
<span data-ttu-id="4b169-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4b169-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b169-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b169-123">CommonParameters</span></span>
<span data-ttu-id="4b169-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b169-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b169-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b169-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b169-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4b169-126">INPUTS</span></span>

### <span data-ttu-id="4b169-127">Instalação</span><span class="sxs-lookup"><span data-stu-id="4b169-127">Site</span></span>
<span data-ttu-id="4b169-128">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="4b169-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="4b169-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4b169-129">OUTPUTS</span></span>

## <span data-ttu-id="4b169-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4b169-130">NOTES</span></span>

## <span data-ttu-id="4b169-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4b169-131">RELATED LINKS</span></span>

