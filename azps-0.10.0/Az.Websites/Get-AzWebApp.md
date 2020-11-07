---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebApp.md
ms.openlocfilehash: f86e0f18c7d793b5876a48c39b56b11c14b17546
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776121"
---
# <span data-ttu-id="df615-101">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="df615-101">Get-AzWebApp</span></span>

## <span data-ttu-id="df615-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="df615-102">SYNOPSIS</span></span>
<span data-ttu-id="df615-103">Obtém os aplicativos Web do Azure no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="df615-103">Gets Azure Web Apps in the specified resource group.</span></span>

## <span data-ttu-id="df615-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="df615-104">SYNTAX</span></span>

### <span data-ttu-id="df615-105">Eles</span><span class="sxs-lookup"><span data-stu-id="df615-105">S1</span></span>
```
Get-AzWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="df615-106">S2</span><span class="sxs-lookup"><span data-stu-id="df615-106">S2</span></span>
```
Get-AzWebApp [-AppServicePlan] <AppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="df615-107">S3</span><span class="sxs-lookup"><span data-stu-id="df615-107">S3</span></span>
```
Get-AzWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df615-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="df615-108">DESCRIPTION</span></span>
<span data-ttu-id="df615-109">O cmdlet **Get-AzWebApp** Obtém informações sobre um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="df615-109">The **Get-AzWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="df615-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="df615-110">EXAMPLES</span></span>

### <span data-ttu-id="df615-111">Exemplo 1: obter um aplicativo Web a partir de um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="df615-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="df615-112">Esse comando obtém o aplicativo Web chamado ContosoSite que pertence ao grupo de recursos Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="df615-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="df615-113">OS</span><span class="sxs-lookup"><span data-stu-id="df615-113">PARAMETERS</span></span>

### <span data-ttu-id="df615-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="df615-114">-AppServicePlan</span></span>
<span data-ttu-id="df615-115">Objeto plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="df615-115">App Service Plan object</span></span>

```yaml
Type: AppServicePlan
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df615-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df615-116">-DefaultProfile</span></span>
<span data-ttu-id="df615-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="df615-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df615-118">-Local</span><span class="sxs-lookup"><span data-stu-id="df615-118">-Location</span></span>
<span data-ttu-id="df615-119">Ponto</span><span class="sxs-lookup"><span data-stu-id="df615-119">Location</span></span>

```yaml
Type: String
Parameter Sets: S3
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df615-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="df615-120">-Name</span></span>
<span data-ttu-id="df615-121">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="df615-121">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df615-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df615-122">-ResourceGroupName</span></span>
<span data-ttu-id="df615-123">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="df615-123">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df615-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df615-124">CommonParameters</span></span>
<span data-ttu-id="df615-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df615-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df615-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df615-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df615-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="df615-127">INPUTS</span></span>

### <span data-ttu-id="df615-128">System. String</span><span class="sxs-lookup"><span data-stu-id="df615-128">System.String</span></span>

## <span data-ttu-id="df615-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="df615-129">OUTPUTS</span></span>

### <span data-ttu-id="df615-130">Microsoft. Azure. Management. WebSites. Models. site</span><span class="sxs-lookup"><span data-stu-id="df615-130">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="df615-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="df615-131">NOTES</span></span>

## <span data-ttu-id="df615-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="df615-132">RELATED LINKS</span></span>

[<span data-ttu-id="df615-133">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="df615-133">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="df615-134">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="df615-134">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="df615-135">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="df615-135">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="df615-136">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="df615-136">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="df615-137">Parar-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="df615-137">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


