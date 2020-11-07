---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
ms.openlocfilehash: 2ba74b42225646507d5bd081300405edfb9410fa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774397"
---
# <span data-ttu-id="2611f-101">Get-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="2611f-101">Get-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="2611f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2611f-102">SYNOPSIS</span></span>
<span data-ttu-id="2611f-103">Obtém um perfil de publicação do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="2611f-103">Gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="2611f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2611f-104">SYNTAX</span></span>

### <span data-ttu-id="2611f-105">Eles</span><span class="sxs-lookup"><span data-stu-id="2611f-105">S1</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2611f-106">S2</span><span class="sxs-lookup"><span data-stu-id="2611f-106">S2</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints]
 [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2611f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2611f-107">DESCRIPTION</span></span>
<span data-ttu-id="2611f-108">O cmdlet **Get-AzWebAppPublishingProfile** Obtém um perfil de publicação do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="2611f-108">The **Get-AzWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="2611f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2611f-109">EXAMPLES</span></span>

### <span data-ttu-id="2611f-110">1:</span><span class="sxs-lookup"><span data-stu-id="2611f-110">1:</span></span>
```
PS C:\> Get-AzWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile.publishsettings"
```

<span data-ttu-id="2611f-111">Este comando obtém o perfil de publicação no formato FTP para o aplicativo Web ContosoWebApp associado ao grupo de recursos Default-Web-Oesteus e o armazena no arquivo de saída especificado.</span><span class="sxs-lookup"><span data-stu-id="2611f-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="2611f-112">OS</span><span class="sxs-lookup"><span data-stu-id="2611f-112">PARAMETERS</span></span>

### <span data-ttu-id="2611f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2611f-113">-DefaultProfile</span></span>
<span data-ttu-id="2611f-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2611f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2611f-115">-Format</span><span class="sxs-lookup"><span data-stu-id="2611f-115">-Format</span></span>
<span data-ttu-id="2611f-116">Format</span><span class="sxs-lookup"><span data-stu-id="2611f-116">Format</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2611f-117">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="2611f-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="2611f-118">Inclua os pontos de extremidade de recuperação de desastre se verdadeiro</span><span class="sxs-lookup"><span data-stu-id="2611f-118">Include the disaster recovery endpoints if true</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2611f-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="2611f-119">-Name</span></span>
<span data-ttu-id="2611f-120">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="2611f-120">WebApp Name</span></span>

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

### <span data-ttu-id="2611f-121">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="2611f-121">-OutputFile</span></span>
<span data-ttu-id="2611f-122">Arquivo de saída</span><span class="sxs-lookup"><span data-stu-id="2611f-122">Output File</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2611f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2611f-123">-ResourceGroupName</span></span>
<span data-ttu-id="2611f-124">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="2611f-124">Resource Group Name</span></span>

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

### <span data-ttu-id="2611f-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="2611f-125">-WebApp</span></span>
<span data-ttu-id="2611f-126">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="2611f-126">WebApp Object</span></span>

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

### <span data-ttu-id="2611f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2611f-127">CommonParameters</span></span>
<span data-ttu-id="2611f-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2611f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2611f-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2611f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2611f-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2611f-130">INPUTS</span></span>

### <span data-ttu-id="2611f-131">System. String</span><span class="sxs-lookup"><span data-stu-id="2611f-131">System.String</span></span>

### <span data-ttu-id="2611f-132">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="2611f-132">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="2611f-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2611f-133">OUTPUTS</span></span>

### <span data-ttu-id="2611f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="2611f-134">System.String</span></span>

## <span data-ttu-id="2611f-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2611f-135">NOTES</span></span>

## <span data-ttu-id="2611f-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2611f-136">RELATED LINKS</span></span>

[<span data-ttu-id="2611f-137">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2611f-137">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="2611f-138">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="2611f-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


