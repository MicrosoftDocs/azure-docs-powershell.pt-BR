---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 8337BEA9-4927-4718-83B9-F3F567BE0FBD
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupConfiguration.md
ms.openlocfilehash: 00df9069400a1d3e2ae10abfb03d9d55bff08735
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887932"
---
# <span data-ttu-id="c2754-101">Get-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="c2754-101">Get-AzWebAppBackupConfiguration</span></span>

## <span data-ttu-id="c2754-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2754-102">SYNOPSIS</span></span>

## <span data-ttu-id="c2754-103">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c2754-103">SYNTAX</span></span>

### <span data-ttu-id="c2754-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="c2754-104">FromResourceName</span></span>
```
Get-AzWebAppBackupConfiguration [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2754-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="c2754-105">FromWebApp</span></span>
```
Get-AzWebAppBackupConfiguration [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c2754-106">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c2754-106">DESCRIPTION</span></span>
<span data-ttu-id="c2754-107">O cmdlet **Get-AzWebAppBackupConfiguration** obtém a configuração de backup de um Aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="c2754-107">The **Get-AzWebAppBackupConfiguration** cmdlet gets the backup configuration of an Azure Web App.</span></span>

## <span data-ttu-id="c2754-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c2754-108">EXAMPLES</span></span>

### <span data-ttu-id="c2754-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c2754-109">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppBackupConfiguration -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="c2754-110">Este comando obtém a configuração de backup do Aplicativo Web chamado WebAppStandard que pertence ao grupo de recursos Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="c2754-110">This command gets the backup configuration from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="c2754-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c2754-111">PARAMETERS</span></span>

### <span data-ttu-id="c2754-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2754-112">-DefaultProfile</span></span>
<span data-ttu-id="c2754-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="c2754-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2754-114">-Name</span><span class="sxs-lookup"><span data-stu-id="c2754-114">-Name</span></span>
<span data-ttu-id="c2754-115">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="c2754-115">WebApp Name</span></span>

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

### <span data-ttu-id="c2754-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2754-116">-ResourceGroupName</span></span>
<span data-ttu-id="c2754-117">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="c2754-117">Resource Group Name</span></span>

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

### <span data-ttu-id="c2754-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="c2754-118">-Slot</span></span>
<span data-ttu-id="c2754-119">Nome do slot</span><span class="sxs-lookup"><span data-stu-id="c2754-119">Slot Name</span></span>

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

### <span data-ttu-id="c2754-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="c2754-120">-WebApp</span></span>
<span data-ttu-id="c2754-121">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="c2754-121">WebApp Name</span></span>

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

### <span data-ttu-id="c2754-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2754-122">CommonParameters</span></span>
<span data-ttu-id="c2754-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2754-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2754-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2754-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2754-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c2754-125">INPUTS</span></span>

### <span data-ttu-id="c2754-126">System.String</span><span class="sxs-lookup"><span data-stu-id="c2754-126">System.String</span></span>

### <span data-ttu-id="c2754-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="c2754-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c2754-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c2754-128">OUTPUTS</span></span>

### <span data-ttu-id="c2754-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="c2754-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="c2754-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="c2754-130">NOTES</span></span>

## <span data-ttu-id="c2754-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c2754-131">RELATED LINKS</span></span>
