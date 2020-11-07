---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappsnapshot
schema: 2.0.0
ms.openlocfilehash: 754ff798ca001e2c6b5a067f6e6244704fc2f617
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785291"
---
# <span data-ttu-id="fa143-101">Get-AzureRmWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="fa143-101">Get-AzureRmWebAppSnapshot</span></span>

## <span data-ttu-id="fa143-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fa143-102">SYNOPSIS</span></span>
<span data-ttu-id="fa143-103">Obtém os instantâneos disponíveis para um aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="fa143-103">Gets the snapshots available for a web app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa143-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fa143-104">SYNTAX</span></span>

### <span data-ttu-id="fa143-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="fa143-105">FromResourceName</span></span>
```
Get-AzureRmWebAppSnapshot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="fa143-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="fa143-106">FromWebApp</span></span>
```
Get-AzureRmWebAppSnapshot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="fa143-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fa143-107">DESCRIPTION</span></span>
<span data-ttu-id="fa143-108">O cmdlet **Get-AzureRmWebAppSnapshot** retorna todos os instantâneos de um aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="fa143-108">The **Get-AzureRmWebAppSnapshot** cmdlet returns all snapshots for a web app.</span></span> <span data-ttu-id="fa143-109">Instantâneos são backups automáticos de arquivos e configurações de um aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="fa143-109">Snapshots are automatic backups of a web app's files and settings.</span></span> <span data-ttu-id="fa143-110">Um instantâneo pode ser restaurado com o cmdlet **Restore-AzureRmWebAppSnapshot** .</span><span class="sxs-lookup"><span data-stu-id="fa143-110">A snapshot can be restored with the **Restore-AzureRmWebAppSnapshot** cmdlet.</span></span>

## <span data-ttu-id="fa143-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fa143-111">EXAMPLES</span></span>

### <span data-ttu-id="fa143-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fa143-112">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

<span data-ttu-id="fa143-113">Obter os instantâneos de um aplicativo Web chamado "ConstosoApp" com um slot chamado "staging" no grupo de recursos "Default-Web-Oesteus"</span><span class="sxs-lookup"><span data-stu-id="fa143-113">Get the snapshots for a web app named "ConstosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group</span></span>

## <span data-ttu-id="fa143-114">OS</span><span class="sxs-lookup"><span data-stu-id="fa143-114">PARAMETERS</span></span>

### <span data-ttu-id="fa143-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa143-115">-DefaultProfile</span></span>
<span data-ttu-id="fa143-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fa143-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa143-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="fa143-117">-Name</span></span>
<span data-ttu-id="fa143-118">O nome do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="fa143-118">The name of the web app.</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa143-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa143-119">-ResourceGroupName</span></span>
<span data-ttu-id="fa143-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fa143-120">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa143-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="fa143-121">-Slot</span></span>
<span data-ttu-id="fa143-122">O nome do slot do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="fa143-122">The name of the web app slot.</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa143-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="fa143-123">-WebApp</span></span>
<span data-ttu-id="fa143-124">O objeto Web App</span><span class="sxs-lookup"><span data-stu-id="fa143-124">The web app object</span></span>

```yaml
Type: Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

## <span data-ttu-id="fa143-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fa143-125">INPUTS</span></span>

### <span data-ttu-id="fa143-126">System. String</span><span class="sxs-lookup"><span data-stu-id="fa143-126">System.String</span></span>
<span data-ttu-id="fa143-127">Microsoft. Azure. Management. WebSites. Models. site</span><span class="sxs-lookup"><span data-stu-id="fa143-127">Microsoft.Azure.Management.WebSites.Models.Site</span></span>


## <span data-ttu-id="fa143-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fa143-128">OUTPUTS</span></span>

### <span data-ttu-id="fa143-129">Microsoft. Azure. Commands. webapps. cmdlets. BackupRestore. AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="fa143-129">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>


## <span data-ttu-id="fa143-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fa143-130">NOTES</span></span>

## <span data-ttu-id="fa143-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fa143-131">RELATED LINKS</span></span>

