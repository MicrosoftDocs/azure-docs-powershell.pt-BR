---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebApp.md
ms.openlocfilehash: 7dc1d2c5d6be1fd920ec9fb4eb90bf73b2c464b9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113128"
---
# <span data-ttu-id="f1c34-101">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f1c34-101">Get-AzWebApp</span></span>

## <span data-ttu-id="f1c34-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f1c34-102">SYNOPSIS</span></span>
<span data-ttu-id="f1c34-103">Obtém os aplicativos Web do Azure no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="f1c34-103">Gets Azure Web Apps in the specified resource group.</span></span>

## <span data-ttu-id="f1c34-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f1c34-104">SYNTAX</span></span>

### <span data-ttu-id="f1c34-105">Eles</span><span class="sxs-lookup"><span data-stu-id="f1c34-105">S1</span></span>
```
Get-AzWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f1c34-106">S2</span><span class="sxs-lookup"><span data-stu-id="f1c34-106">S2</span></span>
```
Get-AzWebApp [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f1c34-107">S3</span><span class="sxs-lookup"><span data-stu-id="f1c34-107">S3</span></span>
```
Get-AzWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1c34-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f1c34-108">DESCRIPTION</span></span>
<span data-ttu-id="f1c34-109">O cmdlet **Get-AzWebApp** Obtém informações sobre um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="f1c34-109">The **Get-AzWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="f1c34-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f1c34-110">EXAMPLES</span></span>

### <span data-ttu-id="f1c34-111">Exemplo 1: obter um aplicativo Web a partir de um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f1c34-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="f1c34-112">Esse comando obtém o aplicativo Web chamado ContosoSite que pertence ao grupo de recursos Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="f1c34-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="f1c34-113">OS</span><span class="sxs-lookup"><span data-stu-id="f1c34-113">PARAMETERS</span></span>

### <span data-ttu-id="f1c34-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="f1c34-114">-AppServicePlan</span></span>
<span data-ttu-id="f1c34-115">Objeto plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="f1c34-115">App Service Plan object</span></span>

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

### <span data-ttu-id="f1c34-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1c34-116">-DefaultProfile</span></span>
<span data-ttu-id="f1c34-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f1c34-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1c34-118">-Local</span><span class="sxs-lookup"><span data-stu-id="f1c34-118">-Location</span></span>
<span data-ttu-id="f1c34-119">Ponto</span><span class="sxs-lookup"><span data-stu-id="f1c34-119">Location</span></span>

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

### <span data-ttu-id="f1c34-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="f1c34-120">-Name</span></span>
<span data-ttu-id="f1c34-121">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="f1c34-121">WebApp Name</span></span>

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

### <span data-ttu-id="f1c34-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1c34-122">-ResourceGroupName</span></span>
<span data-ttu-id="f1c34-123">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f1c34-123">Resource Group Name</span></span>

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

### <span data-ttu-id="f1c34-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1c34-124">CommonParameters</span></span>
<span data-ttu-id="f1c34-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1c34-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1c34-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1c34-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1c34-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f1c34-127">INPUTS</span></span>

### <span data-ttu-id="f1c34-128">System. String</span><span class="sxs-lookup"><span data-stu-id="f1c34-128">System.String</span></span>

## <span data-ttu-id="f1c34-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f1c34-129">OUTPUTS</span></span>

### <span data-ttu-id="f1c34-130">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="f1c34-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="f1c34-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f1c34-131">NOTES</span></span>

## <span data-ttu-id="f1c34-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f1c34-132">RELATED LINKS</span></span>

[<span data-ttu-id="f1c34-133">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f1c34-133">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="f1c34-134">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f1c34-134">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="f1c34-135">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f1c34-135">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="f1c34-136">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f1c34-136">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="f1c34-137">Parar-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f1c34-137">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


