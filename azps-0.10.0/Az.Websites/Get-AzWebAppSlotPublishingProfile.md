---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: B2FDB54F-0318-4037-BC1D-6113E77DDE7E
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: cedaf16333d69a25dce0ce2657640e723767aece
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776101"
---
# <span data-ttu-id="0d2f9-101">Get-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="0d2f9-101">Get-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="0d2f9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0d2f9-102">SYNOPSIS</span></span>
<span data-ttu-id="0d2f9-103">Obtém um perfil de publicação de slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="0d2f9-103">Gets an Azure Web App slot publishing profile.</span></span>

## <span data-ttu-id="0d2f9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0d2f9-104">SYNTAX</span></span>

### <span data-ttu-id="0d2f9-105">Eles</span><span class="sxs-lookup"><span data-stu-id="0d2f9-105">S1</span></span>
```
Get-AzWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0d2f9-106">S2</span><span class="sxs-lookup"><span data-stu-id="0d2f9-106">S2</span></span>
```
Get-AzWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d2f9-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0d2f9-107">DESCRIPTION</span></span>
<span data-ttu-id="0d2f9-108">O cmdlet **Get-AzWebAppSlotPublishingProfile** Obtém o perfil de publicação do aplicativo Web para o slot especificado.</span><span class="sxs-lookup"><span data-stu-id="0d2f9-108">The **Get-AzWebAppSlotPublishingProfile** cmdlet gets the Web App publishing profile for the specified slot.</span></span>

## <span data-ttu-id="0d2f9-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0d2f9-109">EXAMPLES</span></span>

### <span data-ttu-id="0d2f9-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0d2f9-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="0d2f9-111">Esse comando obtém o perfil de publicação no formato FTP para o slot Slot001 pertinente ao ContosoWebApp do aplicativo Web associado ao grupo de recursos Default-Web-Oesteus e o armazena no arquivo de saída especificado.</span><span class="sxs-lookup"><span data-stu-id="0d2f9-111">This command gets the publishing profile in Ftp format for slot Slot001 pertaining to the Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="0d2f9-112">OS</span><span class="sxs-lookup"><span data-stu-id="0d2f9-112">PARAMETERS</span></span>

### <span data-ttu-id="0d2f9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d2f9-113">-DefaultProfile</span></span>
<span data-ttu-id="0d2f9-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0d2f9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d2f9-115">-Format</span><span class="sxs-lookup"><span data-stu-id="0d2f9-115">-Format</span></span>
<span data-ttu-id="0d2f9-116">Format</span><span class="sxs-lookup"><span data-stu-id="0d2f9-116">Format</span></span>

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

### <span data-ttu-id="0d2f9-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="0d2f9-117">-Name</span></span>
<span data-ttu-id="0d2f9-118">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="0d2f9-118">WebApp Name</span></span>

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

### <span data-ttu-id="0d2f9-119">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="0d2f9-119">-OutputFile</span></span>
<span data-ttu-id="0d2f9-120">Arquivo de saída</span><span class="sxs-lookup"><span data-stu-id="0d2f9-120">Output File</span></span>

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

### <span data-ttu-id="0d2f9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d2f9-121">-ResourceGroupName</span></span>
<span data-ttu-id="0d2f9-122">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="0d2f9-122">Resource Group Name</span></span>

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

### <span data-ttu-id="0d2f9-123">-Slot</span><span class="sxs-lookup"><span data-stu-id="0d2f9-123">-Slot</span></span>
<span data-ttu-id="0d2f9-124">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="0d2f9-124">WebApp Slot Name</span></span>

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

### <span data-ttu-id="0d2f9-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="0d2f9-125">-WebApp</span></span>
<span data-ttu-id="0d2f9-126">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="0d2f9-126">WebApp Object</span></span>

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

### <span data-ttu-id="0d2f9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d2f9-127">CommonParameters</span></span>
<span data-ttu-id="0d2f9-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d2f9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d2f9-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d2f9-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d2f9-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0d2f9-130">INPUTS</span></span>

### <span data-ttu-id="0d2f9-131">Instalação</span><span class="sxs-lookup"><span data-stu-id="0d2f9-131">Site</span></span>
<span data-ttu-id="0d2f9-132">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="0d2f9-132">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="0d2f9-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0d2f9-133">OUTPUTS</span></span>

## <span data-ttu-id="0d2f9-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0d2f9-134">NOTES</span></span>

## <span data-ttu-id="0d2f9-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0d2f9-135">RELATED LINKS</span></span>

[<span data-ttu-id="0d2f9-136">Reset-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="0d2f9-136">Reset-AzWebAppSlotPublishingProfile</span></span>](./Reset-AzWebAppSlotPublishingProfile.md)

[<span data-ttu-id="0d2f9-137">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0d2f9-137">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="0d2f9-138">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0d2f9-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
