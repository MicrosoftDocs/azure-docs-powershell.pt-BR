---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: B2FDB54F-0318-4037-BC1D-6113E77DDE7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: 249ecef690fa4eaf59e6a7de97a75d55a285b377
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115590"
---
# <span data-ttu-id="222b5-101">Get-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="222b5-101">Get-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="222b5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="222b5-102">SYNOPSIS</span></span>
<span data-ttu-id="222b5-103">Obtém um perfil de publicação de slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="222b5-103">Gets an Azure Web App slot publishing profile.</span></span>

## <span data-ttu-id="222b5-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="222b5-104">SYNTAX</span></span>

### <span data-ttu-id="222b5-105">S1</span><span class="sxs-lookup"><span data-stu-id="222b5-105">S1</span></span>
```
Get-AzWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="222b5-106">S2</span><span class="sxs-lookup"><span data-stu-id="222b5-106">S2</span></span>
```
Get-AzWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="222b5-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="222b5-107">DESCRIPTION</span></span>
<span data-ttu-id="222b5-108">O cmdlet **Get-AzWebAppSlotPublishingProfile** obtém o perfil de publicação do Web App para o slot especificado.</span><span class="sxs-lookup"><span data-stu-id="222b5-108">The **Get-AzWebAppSlotPublishingProfile** cmdlet gets the Web App publishing profile for the specified slot.</span></span>

## <span data-ttu-id="222b5-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="222b5-109">EXAMPLES</span></span>

### <span data-ttu-id="222b5-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="222b5-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="222b5-111">Esse comando obtém o perfil de publicação no formato Ftp para slot Slot001 pertencente ao Web App ContosoWebApp associado ao grupo de recursos Default-Web-WestUS e o armazena no arquivo de saída especificado.</span><span class="sxs-lookup"><span data-stu-id="222b5-111">This command gets the publishing profile in Ftp format for slot Slot001 pertaining to the Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="222b5-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="222b5-112">PARAMETERS</span></span>

### <span data-ttu-id="222b5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="222b5-113">-DefaultProfile</span></span>
<span data-ttu-id="222b5-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="222b5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="222b5-115">-Formatar</span><span class="sxs-lookup"><span data-stu-id="222b5-115">-Format</span></span>
<span data-ttu-id="222b5-116">Formato</span><span class="sxs-lookup"><span data-stu-id="222b5-116">Format</span></span>

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

### <span data-ttu-id="222b5-117">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="222b5-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="222b5-118">Incluir os pontos de extremidade de recuperação de desastres, se verdadeiro</span><span class="sxs-lookup"><span data-stu-id="222b5-118">Include the disaster recovery endpoints if true</span></span>

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

### <span data-ttu-id="222b5-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="222b5-119">-Name</span></span>
<span data-ttu-id="222b5-120">Nome webapp</span><span class="sxs-lookup"><span data-stu-id="222b5-120">WebApp Name</span></span>

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

### <span data-ttu-id="222b5-121">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="222b5-121">-OutputFile</span></span>
<span data-ttu-id="222b5-122">Arquivo de Saída</span><span class="sxs-lookup"><span data-stu-id="222b5-122">Output File</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="222b5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="222b5-123">-ResourceGroupName</span></span>
<span data-ttu-id="222b5-124">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="222b5-124">Resource Group Name</span></span>

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

### <span data-ttu-id="222b5-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="222b5-125">-Slot</span></span>
<span data-ttu-id="222b5-126">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="222b5-126">WebApp Slot Name</span></span>

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

### <span data-ttu-id="222b5-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="222b5-127">-WebApp</span></span>
<span data-ttu-id="222b5-128">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="222b5-128">WebApp Object</span></span>

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

### <span data-ttu-id="222b5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="222b5-129">CommonParameters</span></span>
<span data-ttu-id="222b5-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="222b5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="222b5-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="222b5-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="222b5-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="222b5-132">INPUTS</span></span>

### <span data-ttu-id="222b5-133">System.String</span><span class="sxs-lookup"><span data-stu-id="222b5-133">System.String</span></span>

### <span data-ttu-id="222b5-134">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="222b5-134">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="222b5-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="222b5-135">OUTPUTS</span></span>

### <span data-ttu-id="222b5-136">System.String</span><span class="sxs-lookup"><span data-stu-id="222b5-136">System.String</span></span>

## <span data-ttu-id="222b5-137">Notas</span><span class="sxs-lookup"><span data-stu-id="222b5-137">NOTES</span></span>

## <span data-ttu-id="222b5-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="222b5-138">RELATED LINKS</span></span>

[<span data-ttu-id="222b5-139">Reset-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="222b5-139">Reset-AzWebAppSlotPublishingProfile</span></span>](./Reset-AzWebAppSlotPublishingProfile.md)

[<span data-ttu-id="222b5-140">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="222b5-140">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="222b5-141">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="222b5-141">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
