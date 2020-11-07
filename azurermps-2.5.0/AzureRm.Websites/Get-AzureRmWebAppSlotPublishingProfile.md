---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: B2FDB54F-0318-4037-BC1D-6113E77DDE7E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslotpublishingprofile
schema: 2.0.0
ms.openlocfilehash: 17ad6612ff36539d212c20c2321c6292fb63a499
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786042"
---
# <span data-ttu-id="1aa37-101">Get-AzureRmWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="1aa37-101">Get-AzureRmWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="1aa37-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1aa37-102">SYNOPSIS</span></span>
<span data-ttu-id="1aa37-103">Obtém um perfil de publicação de slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="1aa37-103">Gets an Azure Web App slot publishing profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1aa37-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1aa37-104">SYNTAX</span></span>

### <span data-ttu-id="1aa37-105">Eles</span><span class="sxs-lookup"><span data-stu-id="1aa37-105">S1</span></span>
```
Get-AzureRmWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1aa37-106">S2</span><span class="sxs-lookup"><span data-stu-id="1aa37-106">S2</span></span>
```
Get-AzureRmWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1aa37-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1aa37-107">DESCRIPTION</span></span>
<span data-ttu-id="1aa37-108">O cmdlet **Get-AzureRmWebAppSlotPublishingProfile** Obtém o perfil de publicação do aplicativo Web para o slot especificado.</span><span class="sxs-lookup"><span data-stu-id="1aa37-108">The **Get-AzureRmWebAppSlotPublishingProfile** cmdlet gets the Web App publishing profile for the specified slot.</span></span>

## <span data-ttu-id="1aa37-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1aa37-109">EXAMPLES</span></span>

### <span data-ttu-id="1aa37-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1aa37-110">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="1aa37-111">Esse comando obtém o perfil de publicação no formato FTP para o slot Slot001 pertinente ao ContosoWebApp do aplicativo Web associado ao grupo de recursos Default-Web-Oesteus e o armazena no arquivo de saída especificado.</span><span class="sxs-lookup"><span data-stu-id="1aa37-111">This command gets the publishing profile in Ftp format for slot Slot001 pertaining to the Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="1aa37-112">OS</span><span class="sxs-lookup"><span data-stu-id="1aa37-112">PARAMETERS</span></span>

### <span data-ttu-id="1aa37-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1aa37-113">-DefaultProfile</span></span>
<span data-ttu-id="1aa37-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1aa37-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1aa37-115">-Format</span><span class="sxs-lookup"><span data-stu-id="1aa37-115">-Format</span></span>
<span data-ttu-id="1aa37-116">Format</span><span class="sxs-lookup"><span data-stu-id="1aa37-116">Format</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aa37-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="1aa37-117">-Name</span></span>
<span data-ttu-id="1aa37-118">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="1aa37-118">WebApp Name</span></span>

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

### <span data-ttu-id="1aa37-119">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="1aa37-119">-OutputFile</span></span>
<span data-ttu-id="1aa37-120">Arquivo de saída</span><span class="sxs-lookup"><span data-stu-id="1aa37-120">Output File</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aa37-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1aa37-121">-ResourceGroupName</span></span>
<span data-ttu-id="1aa37-122">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="1aa37-122">Resource Group Name</span></span>

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

### <span data-ttu-id="1aa37-123">-Slot</span><span class="sxs-lookup"><span data-stu-id="1aa37-123">-Slot</span></span>
<span data-ttu-id="1aa37-124">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="1aa37-124">WebApp Slot Name</span></span>

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

### <span data-ttu-id="1aa37-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="1aa37-125">-WebApp</span></span>
<span data-ttu-id="1aa37-126">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="1aa37-126">WebApp Object</span></span>

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

### <span data-ttu-id="1aa37-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1aa37-127">CommonParameters</span></span>
<span data-ttu-id="1aa37-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1aa37-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1aa37-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1aa37-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1aa37-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1aa37-130">INPUTS</span></span>

### <span data-ttu-id="1aa37-131">Instalação</span><span class="sxs-lookup"><span data-stu-id="1aa37-131">Site</span></span>
<span data-ttu-id="1aa37-132">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="1aa37-132">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="1aa37-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1aa37-133">OUTPUTS</span></span>

## <span data-ttu-id="1aa37-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1aa37-134">NOTES</span></span>

## <span data-ttu-id="1aa37-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1aa37-135">RELATED LINKS</span></span>

[<span data-ttu-id="1aa37-136">Reset-AzureRMWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="1aa37-136">Reset-AzureRMWebAppSlotPublishingProfile</span></span>](./Reset-AzureRmWebAppSlotPublishingProfile.md)

[<span data-ttu-id="1aa37-137">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1aa37-137">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="1aa37-138">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1aa37-138">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
