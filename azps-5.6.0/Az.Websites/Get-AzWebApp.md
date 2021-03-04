---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebApp.md
ms.openlocfilehash: 32e71b33b3c440701e501c4b68d740dcf121001d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889371"
---
# <span data-ttu-id="c08fa-101">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c08fa-101">Get-AzWebApp</span></span>

## <span data-ttu-id="c08fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c08fa-102">SYNOPSIS</span></span>
<span data-ttu-id="c08fa-103">Obtém o Azure Web Apps no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="c08fa-103">Gets Azure Web Apps in the specified resource group.</span></span>

## <span data-ttu-id="c08fa-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c08fa-104">SYNTAX</span></span>

### <span data-ttu-id="c08fa-105">S1</span><span class="sxs-lookup"><span data-stu-id="c08fa-105">S1</span></span>
```
Get-AzWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c08fa-106">S2</span><span class="sxs-lookup"><span data-stu-id="c08fa-106">S2</span></span>
```
Get-AzWebApp [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c08fa-107">S3</span><span class="sxs-lookup"><span data-stu-id="c08fa-107">S3</span></span>
```
Get-AzWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c08fa-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c08fa-108">DESCRIPTION</span></span>
<span data-ttu-id="c08fa-109">O cmdlet **Get-AzWebApp** obtém informações sobre um Aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="c08fa-109">The **Get-AzWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="c08fa-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c08fa-110">EXAMPLES</span></span>

### <span data-ttu-id="c08fa-111">Exemplo 1: Obter um Aplicativo Web de um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="c08fa-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="c08fa-112">Este comando obtém o Aplicativo Web chamado ContosoSite que pertence ao grupo de recursos Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="c08fa-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="c08fa-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c08fa-113">PARAMETERS</span></span>

### <span data-ttu-id="c08fa-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c08fa-114">-AppServicePlan</span></span>
<span data-ttu-id="c08fa-115">Objeto Plano de Serviço de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="c08fa-115">App Service Plan object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c08fa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c08fa-116">-DefaultProfile</span></span>
<span data-ttu-id="c08fa-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="c08fa-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c08fa-118">-Location</span><span class="sxs-lookup"><span data-stu-id="c08fa-118">-Location</span></span>
<span data-ttu-id="c08fa-119">Local</span><span class="sxs-lookup"><span data-stu-id="c08fa-119">Location</span></span>

```yaml
Type: System.String
Parameter Sets: S3
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c08fa-120">-Name</span><span class="sxs-lookup"><span data-stu-id="c08fa-120">-Name</span></span>
<span data-ttu-id="c08fa-121">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="c08fa-121">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c08fa-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c08fa-122">-ResourceGroupName</span></span>
<span data-ttu-id="c08fa-123">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="c08fa-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c08fa-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c08fa-124">CommonParameters</span></span>
<span data-ttu-id="c08fa-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c08fa-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c08fa-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c08fa-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c08fa-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c08fa-127">INPUTS</span></span>

### <span data-ttu-id="c08fa-128">System.String</span><span class="sxs-lookup"><span data-stu-id="c08fa-128">System.String</span></span>

## <span data-ttu-id="c08fa-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c08fa-129">OUTPUTS</span></span>

### <span data-ttu-id="c08fa-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="c08fa-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c08fa-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="c08fa-131">NOTES</span></span>

## <span data-ttu-id="c08fa-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c08fa-132">RELATED LINKS</span></span>

[<span data-ttu-id="c08fa-133">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c08fa-133">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="c08fa-134">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c08fa-134">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="c08fa-135">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c08fa-135">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="c08fa-136">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c08fa-136">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="c08fa-137">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c08fa-137">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


