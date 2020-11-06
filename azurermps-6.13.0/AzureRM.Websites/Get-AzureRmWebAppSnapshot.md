---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSnapshot.md
ms.openlocfilehash: 292364ae6355c640ed66116c84289fe303acdd53
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426245"
---
# <span data-ttu-id="a4317-101">Get-AzureRmWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="a4317-101">Get-AzureRmWebAppSnapshot</span></span>

## <span data-ttu-id="a4317-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a4317-102">SYNOPSIS</span></span>
<span data-ttu-id="a4317-103">Obtém os instantâneos disponíveis para um aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="a4317-103">Gets the snapshots available for a web app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4317-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a4317-104">SYNTAX</span></span>

### <span data-ttu-id="a4317-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="a4317-105">FromResourceName</span></span>
```
Get-AzureRmWebAppSnapshot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4317-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="a4317-106">FromWebApp</span></span>
```
Get-AzureRmWebAppSnapshot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4317-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a4317-107">DESCRIPTION</span></span>
<span data-ttu-id="a4317-108">O cmdlet **Get-AzureRmWebAppSnapshot** retorna todos os instantâneos de um aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="a4317-108">The **Get-AzureRmWebAppSnapshot** cmdlet returns all snapshots for a web app.</span></span> <span data-ttu-id="a4317-109">Instantâneos são backups automáticos de arquivos e configurações de um aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="a4317-109">Snapshots are automatic backups of a web app's files and settings.</span></span> <span data-ttu-id="a4317-110">Um instantâneo pode ser restaurado com o cmdlet **Restore-AzureRmWebAppSnapshot** .</span><span class="sxs-lookup"><span data-stu-id="a4317-110">A snapshot can be restored with the **Restore-AzureRmWebAppSnapshot** cmdlet.</span></span>

## <span data-ttu-id="a4317-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a4317-111">EXAMPLES</span></span>

### <span data-ttu-id="a4317-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a4317-112">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

<span data-ttu-id="a4317-113">Obter os instantâneos de um aplicativo Web chamado "ConstosoApp" com um slot chamado "staging" no grupo de recursos "Default-Web-Oesteus"</span><span class="sxs-lookup"><span data-stu-id="a4317-113">Get the snapshots for a web app named "ConstosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group</span></span>

## <span data-ttu-id="a4317-114">OS</span><span class="sxs-lookup"><span data-stu-id="a4317-114">PARAMETERS</span></span>

### <span data-ttu-id="a4317-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4317-115">-DefaultProfile</span></span>
<span data-ttu-id="a4317-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a4317-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4317-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="a4317-117">-Name</span></span>
<span data-ttu-id="a4317-118">O nome do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="a4317-118">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4317-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4317-119">-ResourceGroupName</span></span>
<span data-ttu-id="a4317-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a4317-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4317-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="a4317-121">-Slot</span></span>
<span data-ttu-id="a4317-122">O nome do slot do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="a4317-122">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4317-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="a4317-123">-WebApp</span></span>
<span data-ttu-id="a4317-124">O objeto Web App</span><span class="sxs-lookup"><span data-stu-id="a4317-124">The web app object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4317-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4317-125">CommonParameters</span></span>
<span data-ttu-id="a4317-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4317-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4317-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4317-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4317-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a4317-128">INPUTS</span></span>

### <span data-ttu-id="a4317-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a4317-129">System.String</span></span>

### <span data-ttu-id="a4317-130">Microsoft. Azure. Management. WebSites. Models. site</span><span class="sxs-lookup"><span data-stu-id="a4317-130">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="a4317-131">Parâmetros: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a4317-131">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="a4317-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a4317-132">OUTPUTS</span></span>

### <span data-ttu-id="a4317-133">Microsoft. Azure. Commands. webapps. cmdlets. BackupRestore. AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="a4317-133">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>

## <span data-ttu-id="a4317-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a4317-134">NOTES</span></span>

## <span data-ttu-id="a4317-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a4317-135">RELATED LINKS</span></span>
