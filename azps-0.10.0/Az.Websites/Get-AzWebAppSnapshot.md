---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
ms.openlocfilehash: 1374bfb67b3150b2c65841d91fd440a83f791b95
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776107"
---
# <span data-ttu-id="0b727-101">Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="0b727-101">Get-AzWebAppSnapshot</span></span>

## <span data-ttu-id="0b727-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0b727-102">SYNOPSIS</span></span>
<span data-ttu-id="0b727-103">Obtém os instantâneos disponíveis para um aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="0b727-103">Gets the snapshots available for a web app.</span></span>

## <span data-ttu-id="0b727-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0b727-104">SYNTAX</span></span>

### <span data-ttu-id="0b727-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="0b727-105">FromResourceName</span></span>
```
Get-AzWebAppSnapshot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="0b727-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="0b727-106">FromWebApp</span></span>
```
Get-AzWebAppSnapshot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="0b727-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0b727-107">DESCRIPTION</span></span>
<span data-ttu-id="0b727-108">O cmdlet **Get-AzWebAppSnapshot** retorna todos os instantâneos de um aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="0b727-108">The **Get-AzWebAppSnapshot** cmdlet returns all snapshots for a web app.</span></span> <span data-ttu-id="0b727-109">Instantâneos são backups automáticos de arquivos e configurações de um aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="0b727-109">Snapshots are automatic backups of a web app's files and settings.</span></span> <span data-ttu-id="0b727-110">Um instantâneo pode ser restaurado com o cmdlet **Restore-AzWebAppSnapshot** .</span><span class="sxs-lookup"><span data-stu-id="0b727-110">A snapshot can be restored with the **Restore-AzWebAppSnapshot** cmdlet.</span></span>

## <span data-ttu-id="0b727-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0b727-111">EXAMPLES</span></span>

### <span data-ttu-id="0b727-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0b727-112">Example 1</span></span>
```
PS C:\> Get-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

<span data-ttu-id="0b727-113">Obter os instantâneos de um aplicativo Web chamado "ConstosoApp" com um slot chamado "staging" no grupo de recursos "Default-Web-Oesteus"</span><span class="sxs-lookup"><span data-stu-id="0b727-113">Get the snapshots for a web app named "ConstosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group</span></span>

## <span data-ttu-id="0b727-114">OS</span><span class="sxs-lookup"><span data-stu-id="0b727-114">PARAMETERS</span></span>

### <span data-ttu-id="0b727-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b727-115">-DefaultProfile</span></span>
<span data-ttu-id="0b727-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0b727-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b727-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="0b727-117">-Name</span></span>
<span data-ttu-id="0b727-118">O nome do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="0b727-118">The name of the web app.</span></span>

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

### <span data-ttu-id="0b727-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b727-119">-ResourceGroupName</span></span>
<span data-ttu-id="0b727-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0b727-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="0b727-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="0b727-121">-Slot</span></span>
<span data-ttu-id="0b727-122">O nome do slot do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="0b727-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="0b727-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="0b727-123">-WebApp</span></span>
<span data-ttu-id="0b727-124">O objeto Web App</span><span class="sxs-lookup"><span data-stu-id="0b727-124">The web app object</span></span>

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

## <span data-ttu-id="0b727-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0b727-125">INPUTS</span></span>

### <span data-ttu-id="0b727-126">System. String</span><span class="sxs-lookup"><span data-stu-id="0b727-126">System.String</span></span>
<span data-ttu-id="0b727-127">Microsoft. Azure. Management. WebSites. Models. site</span><span class="sxs-lookup"><span data-stu-id="0b727-127">Microsoft.Azure.Management.WebSites.Models.Site</span></span>


## <span data-ttu-id="0b727-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0b727-128">OUTPUTS</span></span>

### <span data-ttu-id="0b727-129">Microsoft. Azure. Commands. webapps. cmdlets. BackupRestore. AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="0b727-129">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>


## <span data-ttu-id="0b727-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0b727-130">NOTES</span></span>

## <span data-ttu-id="0b727-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0b727-131">RELATED LINKS</span></span>

