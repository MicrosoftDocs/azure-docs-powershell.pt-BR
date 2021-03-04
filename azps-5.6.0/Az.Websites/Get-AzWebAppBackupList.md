---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebappbackuplist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupList.md
ms.openlocfilehash: f70caa984fde48db6b2d1d147ebf62f544f2ed9f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887933"
---
# <span data-ttu-id="2cc72-101">Get-AzWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="2cc72-101">Get-AzWebAppBackupList</span></span>

## <span data-ttu-id="2cc72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2cc72-102">SYNOPSIS</span></span>

## <span data-ttu-id="2cc72-103">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2cc72-103">SYNTAX</span></span>

### <span data-ttu-id="2cc72-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="2cc72-104">FromResourceName</span></span>
```
Get-AzWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cc72-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="2cc72-105">FromWebApp</span></span>
```
Get-AzWebAppBackupList [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2cc72-106">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2cc72-106">DESCRIPTION</span></span>
<span data-ttu-id="2cc72-107">O cmdlet **Get-AzWebAppBackupList** obtém uma lista de backups para um Aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="2cc72-107">The **Get-AzWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="2cc72-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2cc72-108">EXAMPLES</span></span>

### <span data-ttu-id="2cc72-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2cc72-109">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="2cc72-110">Este comando retorna uma lista de backup pertencente a WebApp WebAppStandard associada ao grupo de recursos ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2cc72-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="2cc72-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2cc72-111">PARAMETERS</span></span>

### <span data-ttu-id="2cc72-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cc72-112">-DefaultProfile</span></span>
<span data-ttu-id="2cc72-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="2cc72-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2cc72-114">-Name</span><span class="sxs-lookup"><span data-stu-id="2cc72-114">-Name</span></span>
<span data-ttu-id="2cc72-115">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="2cc72-115">WebApp Name</span></span>

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

### <span data-ttu-id="2cc72-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cc72-116">-ResourceGroupName</span></span>
<span data-ttu-id="2cc72-117">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="2cc72-117">Resource Group Name</span></span>

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

### <span data-ttu-id="2cc72-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="2cc72-118">-Slot</span></span>
<span data-ttu-id="2cc72-119">Nome do slot</span><span class="sxs-lookup"><span data-stu-id="2cc72-119">Slot name</span></span>

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

### <span data-ttu-id="2cc72-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="2cc72-120">-WebApp</span></span>
<span data-ttu-id="2cc72-121">WebApp canalizou</span><span class="sxs-lookup"><span data-stu-id="2cc72-121">Piped WebApp</span></span>

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

### <span data-ttu-id="2cc72-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cc72-122">CommonParameters</span></span>
<span data-ttu-id="2cc72-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cc72-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cc72-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cc72-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cc72-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2cc72-125">INPUTS</span></span>

### <span data-ttu-id="2cc72-126">System.String</span><span class="sxs-lookup"><span data-stu-id="2cc72-126">System.String</span></span>

### <span data-ttu-id="2cc72-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="2cc72-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="2cc72-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2cc72-128">OUTPUTS</span></span>

### <span data-ttu-id="2cc72-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="2cc72-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="2cc72-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="2cc72-130">NOTES</span></span>

## <span data-ttu-id="2cc72-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2cc72-131">RELATED LINKS</span></span>
