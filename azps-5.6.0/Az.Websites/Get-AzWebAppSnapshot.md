---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
ms.openlocfilehash: 14567157501b81ba669061285025ba1631be88d4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888771"
---
# <span data-ttu-id="b5dfd-101">Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="b5dfd-101">Get-AzWebAppSnapshot</span></span>

## <span data-ttu-id="b5dfd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5dfd-102">SYNOPSIS</span></span>
<span data-ttu-id="b5dfd-103">Obtém os instantâneos disponíveis para um aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="b5dfd-103">Gets the snapshots available for a web app.</span></span>

## <span data-ttu-id="b5dfd-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b5dfd-104">SYNTAX</span></span>

### <span data-ttu-id="b5dfd-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="b5dfd-105">FromResourceName</span></span>
```
Get-AzWebAppSnapshot [-UseDisasterRecovery] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5dfd-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="b5dfd-106">FromWebApp</span></span>
```
Get-AzWebAppSnapshot [-UseDisasterRecovery] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b5dfd-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b5dfd-107">DESCRIPTION</span></span>
<span data-ttu-id="b5dfd-108">O cmdlet **Get-AzWebAppSnapshot** retorna todos os instantâneos de um aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="b5dfd-108">The **Get-AzWebAppSnapshot** cmdlet returns all snapshots for a web app.</span></span> <span data-ttu-id="b5dfd-109">Instantâneos são backups automáticos de arquivos e configurações de um aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="b5dfd-109">Snapshots are automatic backups of a web app's files and settings.</span></span> <span data-ttu-id="b5dfd-110">Um instantâneo pode ser restaurado com o cmdlet **Restore-AzWebAppSnapshot.**</span><span class="sxs-lookup"><span data-stu-id="b5dfd-110">A snapshot can be restored with the **Restore-AzWebAppSnapshot** cmdlet.</span></span>

## <span data-ttu-id="b5dfd-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b5dfd-111">EXAMPLES</span></span>

### <span data-ttu-id="b5dfd-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b5dfd-112">Example 1</span></span>
```
PS C:\> Get-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

<span data-ttu-id="b5dfd-113">Obter os instantâneos de um aplicativo Web chamado "ContosoApp" com um slot chamado "Preparação" no grupo de recursos "Default-Web-WestUS"</span><span class="sxs-lookup"><span data-stu-id="b5dfd-113">Get the snapshots for a web app named "ContosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group</span></span>

## <span data-ttu-id="b5dfd-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b5dfd-114">PARAMETERS</span></span>

### <span data-ttu-id="b5dfd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5dfd-115">-DefaultProfile</span></span>
<span data-ttu-id="b5dfd-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b5dfd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5dfd-117">-Name</span><span class="sxs-lookup"><span data-stu-id="b5dfd-117">-Name</span></span>
<span data-ttu-id="b5dfd-118">O nome do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="b5dfd-118">The name of the web app.</span></span>

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

### <span data-ttu-id="b5dfd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5dfd-119">-ResourceGroupName</span></span>
<span data-ttu-id="b5dfd-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b5dfd-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="b5dfd-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="b5dfd-121">-Slot</span></span>
<span data-ttu-id="b5dfd-122">O nome do slot do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="b5dfd-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="b5dfd-123">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="b5dfd-123">-UseDisasterRecovery</span></span>
<span data-ttu-id="b5dfd-124">Leia os instantâneos de uma unidade de escala secundária.</span><span class="sxs-lookup"><span data-stu-id="b5dfd-124">Read the snapshots from a secondary scale unit.</span></span>

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

### <span data-ttu-id="b5dfd-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="b5dfd-125">-WebApp</span></span>
<span data-ttu-id="b5dfd-126">O objeto do aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="b5dfd-126">The web app object</span></span>

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

### <span data-ttu-id="b5dfd-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5dfd-127">CommonParameters</span></span>
<span data-ttu-id="b5dfd-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5dfd-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5dfd-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5dfd-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5dfd-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b5dfd-130">INPUTS</span></span>

### <span data-ttu-id="b5dfd-131">System.String</span><span class="sxs-lookup"><span data-stu-id="b5dfd-131">System.String</span></span>

### <span data-ttu-id="b5dfd-132">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="b5dfd-132">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="b5dfd-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b5dfd-133">OUTPUTS</span></span>

### <span data-ttu-id="b5dfd-134">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="b5dfd-134">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>

## <span data-ttu-id="b5dfd-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="b5dfd-135">NOTES</span></span>

## <span data-ttu-id="b5dfd-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b5dfd-136">RELATED LINKS</span></span>
