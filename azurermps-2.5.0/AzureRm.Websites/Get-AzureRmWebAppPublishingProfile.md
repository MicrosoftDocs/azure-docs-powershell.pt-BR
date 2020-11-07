---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebapppublishingprofile
schema: 2.0.0
ms.openlocfilehash: 5884092a7520517844d6d0137023f99dc744cb86
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785407"
---
# <span data-ttu-id="5f384-101">Get-AzureRmWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="5f384-101">Get-AzureRmWebAppPublishingProfile</span></span>

## <span data-ttu-id="5f384-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5f384-102">SYNOPSIS</span></span>
<span data-ttu-id="5f384-103">Obtém um perfil de publicação do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="5f384-103">Gets an Azure Web App publishing profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f384-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5f384-104">SYNTAX</span></span>

### <span data-ttu-id="5f384-105">Eles</span><span class="sxs-lookup"><span data-stu-id="5f384-105">S1</span></span>
```
Get-AzureRmWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f384-106">S2</span><span class="sxs-lookup"><span data-stu-id="5f384-106">S2</span></span>
```
Get-AzureRmWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f384-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5f384-107">DESCRIPTION</span></span>
<span data-ttu-id="5f384-108">O cmdlet **Get-AzureRmWebAppPublishingProfile** Obtém um perfil de publicação do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="5f384-108">The **Get-AzureRmWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="5f384-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5f384-109">EXAMPLES</span></span>

### <span data-ttu-id="5f384-110">1:</span><span class="sxs-lookup"><span data-stu-id="5f384-110">1:</span></span>
```
PS C:\> Get-AzureRmWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="5f384-111">Este comando obtém o perfil de publicação no formato FTP para o aplicativo Web ContosoWebApp associado ao grupo de recursos Default-Web-Oesteus e o armazena no arquivo de saída especificado.</span><span class="sxs-lookup"><span data-stu-id="5f384-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="5f384-112">OS</span><span class="sxs-lookup"><span data-stu-id="5f384-112">PARAMETERS</span></span>

### <span data-ttu-id="5f384-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f384-113">-DefaultProfile</span></span>
<span data-ttu-id="5f384-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5f384-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f384-115">-Format</span><span class="sxs-lookup"><span data-stu-id="5f384-115">-Format</span></span>
<span data-ttu-id="5f384-116">Format</span><span class="sxs-lookup"><span data-stu-id="5f384-116">Format</span></span>

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

### <span data-ttu-id="5f384-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="5f384-117">-Name</span></span>
<span data-ttu-id="5f384-118">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="5f384-118">WebApp Name</span></span>

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

### <span data-ttu-id="5f384-119">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="5f384-119">-OutputFile</span></span>
<span data-ttu-id="5f384-120">Arquivo de saída</span><span class="sxs-lookup"><span data-stu-id="5f384-120">Output File</span></span>

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

### <span data-ttu-id="5f384-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f384-121">-ResourceGroupName</span></span>
<span data-ttu-id="5f384-122">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="5f384-122">Resource Group Name</span></span>

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

### <span data-ttu-id="5f384-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="5f384-123">-WebApp</span></span>
<span data-ttu-id="5f384-124">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="5f384-124">WebApp Object</span></span>

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

### <span data-ttu-id="5f384-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f384-125">CommonParameters</span></span>
<span data-ttu-id="5f384-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f384-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f384-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f384-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f384-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5f384-128">INPUTS</span></span>

### <span data-ttu-id="5f384-129">Instalação</span><span class="sxs-lookup"><span data-stu-id="5f384-129">Site</span></span>
<span data-ttu-id="5f384-130">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="5f384-130">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="5f384-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5f384-131">OUTPUTS</span></span>

## <span data-ttu-id="5f384-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5f384-132">NOTES</span></span>

## <span data-ttu-id="5f384-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5f384-133">RELATED LINKS</span></span>

[<span data-ttu-id="5f384-134">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="5f384-134">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="5f384-135">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="5f384-135">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


