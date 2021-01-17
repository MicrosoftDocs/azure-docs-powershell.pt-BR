---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
ms.openlocfilehash: 350f7d5b44f5a1c84f97511a4febb7d967ee2de4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427820"
---
# <span data-ttu-id="978d6-101">Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="978d6-101">Get-AzWebAppSnapshot</span></span>

## <span data-ttu-id="978d6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="978d6-102">SYNOPSIS</span></span>
<span data-ttu-id="978d6-103">Obtém os instantâneos disponíveis para um aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="978d6-103">Gets the snapshots available for a web app.</span></span>

## <span data-ttu-id="978d6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="978d6-104">SYNTAX</span></span>

### <span data-ttu-id="978d6-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="978d6-105">FromResourceName</span></span>
```
Get-AzWebAppSnapshot [-UseDisasterRecovery] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="978d6-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="978d6-106">FromWebApp</span></span>
```
Get-AzWebAppSnapshot [-UseDisasterRecovery] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="978d6-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="978d6-107">DESCRIPTION</span></span>
<span data-ttu-id="978d6-108">O cmdlet **Get-AzWebAppSnapshot** retorna todos os instantâneos de um aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="978d6-108">The **Get-AzWebAppSnapshot** cmdlet returns all snapshots for a web app.</span></span> <span data-ttu-id="978d6-109">Instantâneos são backups automáticos de arquivos e configurações de um aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="978d6-109">Snapshots are automatic backups of a web app's files and settings.</span></span> <span data-ttu-id="978d6-110">Um instantâneo pode ser restaurado com o cmdlet **Restore-AzWebAppSnapshot** .</span><span class="sxs-lookup"><span data-stu-id="978d6-110">A snapshot can be restored with the **Restore-AzWebAppSnapshot** cmdlet.</span></span>

## <span data-ttu-id="978d6-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="978d6-111">EXAMPLES</span></span>

### <span data-ttu-id="978d6-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="978d6-112">Example 1</span></span>
```
PS C:\> Get-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

<span data-ttu-id="978d6-113">Obter os instantâneos de um aplicativo Web chamado "ContosoApp" com um slot chamado "staging" no grupo de recursos "Default-Web-Oesteus"</span><span class="sxs-lookup"><span data-stu-id="978d6-113">Get the snapshots for a web app named "ContosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group</span></span>

## <span data-ttu-id="978d6-114">OS</span><span class="sxs-lookup"><span data-stu-id="978d6-114">PARAMETERS</span></span>

### <span data-ttu-id="978d6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="978d6-115">-DefaultProfile</span></span>
<span data-ttu-id="978d6-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="978d6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="978d6-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="978d6-117">-Name</span></span>
<span data-ttu-id="978d6-118">O nome do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="978d6-118">The name of the web app.</span></span>

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

### <span data-ttu-id="978d6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="978d6-119">-ResourceGroupName</span></span>
<span data-ttu-id="978d6-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="978d6-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="978d6-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="978d6-121">-Slot</span></span>
<span data-ttu-id="978d6-122">O nome do slot do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="978d6-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="978d6-123">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="978d6-123">-UseDisasterRecovery</span></span>
<span data-ttu-id="978d6-124">Leia os instantâneos a partir de uma unidade de escala secundária.</span><span class="sxs-lookup"><span data-stu-id="978d6-124">Read the snapshots from a secondary scale unit.</span></span>

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

### <span data-ttu-id="978d6-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="978d6-125">-WebApp</span></span>
<span data-ttu-id="978d6-126">O objeto Web App</span><span class="sxs-lookup"><span data-stu-id="978d6-126">The web app object</span></span>

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

### <span data-ttu-id="978d6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="978d6-127">CommonParameters</span></span>
<span data-ttu-id="978d6-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="978d6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="978d6-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="978d6-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="978d6-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="978d6-130">INPUTS</span></span>

### <span data-ttu-id="978d6-131">System. String</span><span class="sxs-lookup"><span data-stu-id="978d6-131">System.String</span></span>

### <span data-ttu-id="978d6-132">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="978d6-132">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="978d6-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="978d6-133">OUTPUTS</span></span>

### <span data-ttu-id="978d6-134">Microsoft. Azure. Commands. webapps. cmdlets. BackupRestore. AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="978d6-134">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>

## <span data-ttu-id="978d6-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="978d6-135">NOTES</span></span>

## <span data-ttu-id="978d6-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="978d6-136">RELATED LINKS</span></span>
