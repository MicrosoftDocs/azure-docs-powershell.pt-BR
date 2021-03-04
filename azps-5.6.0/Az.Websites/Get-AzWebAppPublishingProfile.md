---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
ms.openlocfilehash: 512162485b38d6cf02ad8519131eb4252605c4a9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891070"
---
# <span data-ttu-id="f7be6-101">Get-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="f7be6-101">Get-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="f7be6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7be6-102">SYNOPSIS</span></span>
<span data-ttu-id="f7be6-103">Obtém um perfil de publicação do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="f7be6-103">Gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="f7be6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f7be6-104">SYNTAX</span></span>

### <span data-ttu-id="f7be6-105">S1</span><span class="sxs-lookup"><span data-stu-id="f7be6-105">S1</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7be6-106">S2</span><span class="sxs-lookup"><span data-stu-id="f7be6-106">S2</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints]
 [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7be6-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f7be6-107">DESCRIPTION</span></span>
<span data-ttu-id="f7be6-108">O cmdlet **Get-AzWebAppPublishingProfile** obtém um perfil de publicação do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="f7be6-108">The **Get-AzWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="f7be6-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f7be6-109">EXAMPLES</span></span>

### <span data-ttu-id="f7be6-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f7be6-110">Example 1</span></span>
```powershell
PS C:\> Get-AzWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile.publishsettings"
```

<span data-ttu-id="f7be6-111">Este comando obtém o perfil de publicação no formato Ftp para Web App ContosoWebApp associado ao grupo de recursos Default-Web-WestUS e o armazena no arquivo de saída especificado.</span><span class="sxs-lookup"><span data-stu-id="f7be6-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="f7be6-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f7be6-112">PARAMETERS</span></span>

### <span data-ttu-id="f7be6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7be6-113">-DefaultProfile</span></span>
<span data-ttu-id="f7be6-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="f7be6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7be6-115">-Format</span><span class="sxs-lookup"><span data-stu-id="f7be6-115">-Format</span></span>
<span data-ttu-id="f7be6-116">Format</span><span class="sxs-lookup"><span data-stu-id="f7be6-116">Format</span></span>

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

### <span data-ttu-id="f7be6-117">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="f7be6-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="f7be6-118">Incluir os pontos de extremidade de recuperação de desastres se for verdadeiro</span><span class="sxs-lookup"><span data-stu-id="f7be6-118">Include the disaster recovery endpoints if true</span></span>

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

### <span data-ttu-id="f7be6-119">-Name</span><span class="sxs-lookup"><span data-stu-id="f7be6-119">-Name</span></span>
<span data-ttu-id="f7be6-120">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="f7be6-120">WebApp Name</span></span>

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

### <span data-ttu-id="f7be6-121">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="f7be6-121">-OutputFile</span></span>
<span data-ttu-id="f7be6-122">Arquivo de saída</span><span class="sxs-lookup"><span data-stu-id="f7be6-122">Output File</span></span>

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

### <span data-ttu-id="f7be6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7be6-123">-ResourceGroupName</span></span>
<span data-ttu-id="f7be6-124">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="f7be6-124">Resource Group Name</span></span>

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

### <span data-ttu-id="f7be6-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="f7be6-125">-WebApp</span></span>
<span data-ttu-id="f7be6-126">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="f7be6-126">WebApp Object</span></span>

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

### <span data-ttu-id="f7be6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7be6-127">CommonParameters</span></span>
<span data-ttu-id="f7be6-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7be6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7be6-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7be6-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7be6-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f7be6-130">INPUTS</span></span>

### <span data-ttu-id="f7be6-131">System.String</span><span class="sxs-lookup"><span data-stu-id="f7be6-131">System.String</span></span>

### <span data-ttu-id="f7be6-132">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="f7be6-132">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="f7be6-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f7be6-133">OUTPUTS</span></span>

### <span data-ttu-id="f7be6-134">System.String</span><span class="sxs-lookup"><span data-stu-id="f7be6-134">System.String</span></span>

## <span data-ttu-id="f7be6-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="f7be6-135">NOTES</span></span>

## <span data-ttu-id="f7be6-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f7be6-136">RELATED LINKS</span></span>

[<span data-ttu-id="f7be6-137">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="f7be6-137">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="f7be6-138">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f7be6-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


