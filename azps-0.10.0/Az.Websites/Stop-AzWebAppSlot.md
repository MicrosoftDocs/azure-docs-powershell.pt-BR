---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 86E0D477-DD32-49BD-82E7-1CF191E4F612
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/stop-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Stop-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Stop-AzWebAppSlot.md
ms.openlocfilehash: 4ac4482cb5972553b1dad3972200d2f0eb032fe4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776046"
---
# <span data-ttu-id="b88b8-101">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b88b8-101">Stop-AzWebAppSlot</span></span>

## <span data-ttu-id="b88b8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b88b8-102">SYNOPSIS</span></span>
<span data-ttu-id="b88b8-103">Interrompe um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="b88b8-103">Stops an Azure Web App slot.</span></span>

## <span data-ttu-id="b88b8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b88b8-104">SYNTAX</span></span>

### <span data-ttu-id="b88b8-105">Eles</span><span class="sxs-lookup"><span data-stu-id="b88b8-105">S1</span></span>
```
Stop-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b88b8-106">S2</span><span class="sxs-lookup"><span data-stu-id="b88b8-106">S2</span></span>
```
Stop-AzWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b88b8-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b88b8-107">DESCRIPTION</span></span>
<span data-ttu-id="b88b8-108">O cmdlet **Stop-AzWebAppSlot** interrompe um slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="b88b8-108">The **Stop-AzWebAppSlot** cmdlet stops an Azure Web App Slot.</span></span>

## <span data-ttu-id="b88b8-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b88b8-109">EXAMPLES</span></span>

### <span data-ttu-id="b88b8-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b88b8-110">Example 1</span></span>
```
PS C:\>Stop-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="b88b8-111">Esse comando interrompe o slot Slot001 pertencente ao aplicativo Web chamado ContosoWebApp que pertence ao grupo de recursos chamado Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="b88b8-111">This command stops the slot Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="b88b8-112">OS</span><span class="sxs-lookup"><span data-stu-id="b88b8-112">PARAMETERS</span></span>

### <span data-ttu-id="b88b8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b88b8-113">-DefaultProfile</span></span>
<span data-ttu-id="b88b8-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b88b8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b88b8-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="b88b8-115">-Name</span></span>
<span data-ttu-id="b88b8-116">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="b88b8-116">WebApp Name</span></span>

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

### <span data-ttu-id="b88b8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b88b8-117">-ResourceGroupName</span></span>
<span data-ttu-id="b88b8-118">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="b88b8-118">Resource Group Name</span></span>

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

### <span data-ttu-id="b88b8-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="b88b8-119">-Slot</span></span>
<span data-ttu-id="b88b8-120">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="b88b8-120">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b88b8-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="b88b8-121">-WebApp</span></span>
<span data-ttu-id="b88b8-122">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="b88b8-122">WebApp Object</span></span>

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

### <span data-ttu-id="b88b8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b88b8-123">CommonParameters</span></span>
<span data-ttu-id="b88b8-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b88b8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b88b8-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b88b8-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b88b8-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b88b8-126">INPUTS</span></span>

### <span data-ttu-id="b88b8-127">Instalação</span><span class="sxs-lookup"><span data-stu-id="b88b8-127">Site</span></span>
<span data-ttu-id="b88b8-128">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="b88b8-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="b88b8-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b88b8-129">OUTPUTS</span></span>

## <span data-ttu-id="b88b8-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b88b8-130">NOTES</span></span>

## <span data-ttu-id="b88b8-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b88b8-131">RELATED LINKS</span></span>

