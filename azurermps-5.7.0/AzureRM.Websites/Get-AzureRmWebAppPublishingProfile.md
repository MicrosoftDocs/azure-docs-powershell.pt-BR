---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppPublishingProfile.md
ms.openlocfilehash: 1202d15504717052513f1ef77a21e008fefe20af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427382"
---
# <span data-ttu-id="18665-101">Get-AzureRmWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="18665-101">Get-AzureRmWebAppPublishingProfile</span></span>

## <span data-ttu-id="18665-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="18665-102">SYNOPSIS</span></span>
<span data-ttu-id="18665-103">Obtém um perfil de publicação do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="18665-103">Gets an Azure Web App publishing profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18665-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="18665-104">SYNTAX</span></span>

### <span data-ttu-id="18665-105">Eles</span><span class="sxs-lookup"><span data-stu-id="18665-105">S1</span></span>
```
Get-AzureRmWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18665-106">S2</span><span class="sxs-lookup"><span data-stu-id="18665-106">S2</span></span>
```
Get-AzureRmWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18665-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="18665-107">DESCRIPTION</span></span>
<span data-ttu-id="18665-108">O cmdlet **Get-AzureRmWebAppPublishingProfile** Obtém um perfil de publicação do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="18665-108">The **Get-AzureRmWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="18665-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="18665-109">EXAMPLES</span></span>

### <span data-ttu-id="18665-110">1:</span><span class="sxs-lookup"><span data-stu-id="18665-110">1:</span></span>
```
PS C:\> Get-AzureRmWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="18665-111">Este comando obtém o perfil de publicação no formato FTP para o aplicativo Web ContosoWebApp associado ao grupo de recursos Default-Web-Oesteus e o armazena no arquivo de saída especificado.</span><span class="sxs-lookup"><span data-stu-id="18665-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="18665-112">OS</span><span class="sxs-lookup"><span data-stu-id="18665-112">PARAMETERS</span></span>

### <span data-ttu-id="18665-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18665-113">-DefaultProfile</span></span>
<span data-ttu-id="18665-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="18665-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18665-115">-Format</span><span class="sxs-lookup"><span data-stu-id="18665-115">-Format</span></span>
<span data-ttu-id="18665-116">Format</span><span class="sxs-lookup"><span data-stu-id="18665-116">Format</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18665-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="18665-117">-Name</span></span>
<span data-ttu-id="18665-118">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="18665-118">WebApp Name</span></span>

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

### <span data-ttu-id="18665-119">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="18665-119">-OutputFile</span></span>
<span data-ttu-id="18665-120">Arquivo de saída</span><span class="sxs-lookup"><span data-stu-id="18665-120">Output File</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18665-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18665-121">-ResourceGroupName</span></span>
<span data-ttu-id="18665-122">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="18665-122">Resource Group Name</span></span>

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

### <span data-ttu-id="18665-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="18665-123">-WebApp</span></span>
<span data-ttu-id="18665-124">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="18665-124">WebApp Object</span></span>

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

### <span data-ttu-id="18665-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18665-125">CommonParameters</span></span>
<span data-ttu-id="18665-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18665-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18665-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18665-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18665-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="18665-128">INPUTS</span></span>

### <span data-ttu-id="18665-129">Instalação</span><span class="sxs-lookup"><span data-stu-id="18665-129">Site</span></span>
<span data-ttu-id="18665-130">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="18665-130">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="18665-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="18665-131">OUTPUTS</span></span>

## <span data-ttu-id="18665-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="18665-132">NOTES</span></span>

## <span data-ttu-id="18665-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="18665-133">RELATED LINKS</span></span>

[<span data-ttu-id="18665-134">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="18665-134">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="18665-135">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="18665-135">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


