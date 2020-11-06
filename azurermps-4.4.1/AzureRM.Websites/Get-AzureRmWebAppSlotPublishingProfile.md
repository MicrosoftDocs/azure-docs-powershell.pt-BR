---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: B2FDB54F-0318-4037-BC1D-6113E77DDE7E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotPublishingProfile.md
ms.openlocfilehash: d8ccd8f1011a73068c24323bb86e39340dfc9573
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429930"
---
# <span data-ttu-id="c22e8-101">Get-AzureRmWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="c22e8-101">Get-AzureRmWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="c22e8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c22e8-102">SYNOPSIS</span></span>
<span data-ttu-id="c22e8-103">Obtém um perfil de publicação de slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="c22e8-103">Gets an Azure Web App slot publishing profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c22e8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c22e8-104">SYNTAX</span></span>

### <span data-ttu-id="c22e8-105">Eles</span><span class="sxs-lookup"><span data-stu-id="c22e8-105">S1</span></span>
```
Get-AzureRmWebAppSlotPublishingProfile [-OutputFile] <String> [[-Format] <String>]
 [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c22e8-106">S2</span><span class="sxs-lookup"><span data-stu-id="c22e8-106">S2</span></span>
```
Get-AzureRmWebAppSlotPublishingProfile [-OutputFile] <String> [[-Format] <String>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c22e8-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c22e8-107">DESCRIPTION</span></span>
<span data-ttu-id="c22e8-108">O cmdlet **Get-AzureRmWebAppSlotPublishingProfile** Obtém o perfil de publicação do aplicativo Web para o slot especificado.</span><span class="sxs-lookup"><span data-stu-id="c22e8-108">The **Get-AzureRmWebAppSlotPublishingProfile** cmdlet gets the Web App publishing profile for the specified slot.</span></span>

## <span data-ttu-id="c22e8-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c22e8-109">EXAMPLES</span></span>

### <span data-ttu-id="c22e8-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c22e8-110">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="c22e8-111">Esse comando obtém o perfil de publicação no formato FTP para o slot Slot001 pertinente ao ContosoWebApp do aplicativo Web associado ao grupo de recursos Default-Web-Oesteus e o armazena no arquivo de saída especificado.</span><span class="sxs-lookup"><span data-stu-id="c22e8-111">This command gets the publishing profile in Ftp format for slot Slot001 pertaining to the Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="c22e8-112">OS</span><span class="sxs-lookup"><span data-stu-id="c22e8-112">PARAMETERS</span></span>

### <span data-ttu-id="c22e8-113">-Format</span><span class="sxs-lookup"><span data-stu-id="c22e8-113">-Format</span></span>
<span data-ttu-id="c22e8-114">Format</span><span class="sxs-lookup"><span data-stu-id="c22e8-114">Format</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c22e8-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="c22e8-115">-Name</span></span>
<span data-ttu-id="c22e8-116">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="c22e8-116">WebApp Name</span></span>

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

### <span data-ttu-id="c22e8-117">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="c22e8-117">-OutputFile</span></span>
<span data-ttu-id="c22e8-118">Arquivo de saída</span><span class="sxs-lookup"><span data-stu-id="c22e8-118">Output File</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c22e8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c22e8-119">-ResourceGroupName</span></span>
<span data-ttu-id="c22e8-120">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="c22e8-120">Resource Group Name</span></span>

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

### <span data-ttu-id="c22e8-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="c22e8-121">-Slot</span></span>
<span data-ttu-id="c22e8-122">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="c22e8-122">WebApp Slot Name</span></span>

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

### <span data-ttu-id="c22e8-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="c22e8-123">-WebApp</span></span>
<span data-ttu-id="c22e8-124">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="c22e8-124">WebApp Object</span></span>

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

### <span data-ttu-id="c22e8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c22e8-125">-DefaultProfile</span></span>
<span data-ttu-id="c22e8-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c22e8-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c22e8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c22e8-127">CommonParameters</span></span>
<span data-ttu-id="c22e8-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c22e8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c22e8-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c22e8-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c22e8-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c22e8-130">INPUTS</span></span>

### <span data-ttu-id="c22e8-131">Instalação</span><span class="sxs-lookup"><span data-stu-id="c22e8-131">Site</span></span>
<span data-ttu-id="c22e8-132">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="c22e8-132">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="c22e8-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c22e8-133">OUTPUTS</span></span>

## <span data-ttu-id="c22e8-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c22e8-134">NOTES</span></span>

## <span data-ttu-id="c22e8-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c22e8-135">RELATED LINKS</span></span>

[<span data-ttu-id="c22e8-136">Reset-AzureRMWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="c22e8-136">Reset-AzureRMWebAppSlotPublishingProfile</span></span>](./Reset-AzureRmWebAppSlotPublishingProfile.md)

[<span data-ttu-id="c22e8-137">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c22e8-137">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="c22e8-138">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c22e8-138">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
