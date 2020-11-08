---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappbackuplist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupList.md
ms.openlocfilehash: 6ea805f1e3a3711c2efe6faefd73edf06c4b51fd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112009"
---
# <span data-ttu-id="90d93-101">Get-AzWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="90d93-101">Get-AzWebAppBackupList</span></span>

## <span data-ttu-id="90d93-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="90d93-102">SYNOPSIS</span></span>

## <span data-ttu-id="90d93-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="90d93-103">SYNTAX</span></span>

### <span data-ttu-id="90d93-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="90d93-104">FromResourceName</span></span>
```
Get-AzWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90d93-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="90d93-105">FromWebApp</span></span>
```
Get-AzWebAppBackupList [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90d93-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="90d93-106">DESCRIPTION</span></span>
<span data-ttu-id="90d93-107">O cmdlet **Get-AzWebAppBackupList** Obtém uma lista de backups para um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="90d93-107">The **Get-AzWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="90d93-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="90d93-108">EXAMPLES</span></span>

### <span data-ttu-id="90d93-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="90d93-109">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="90d93-110">Esse comando retorna uma lista de backup relacionada a WebApp WebAppStandard associada à ContosoResourceGroup do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="90d93-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="90d93-111">OS</span><span class="sxs-lookup"><span data-stu-id="90d93-111">PARAMETERS</span></span>

### <span data-ttu-id="90d93-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90d93-112">-DefaultProfile</span></span>
<span data-ttu-id="90d93-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="90d93-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90d93-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="90d93-114">-Name</span></span>
<span data-ttu-id="90d93-115">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="90d93-115">WebApp Name</span></span>

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

### <span data-ttu-id="90d93-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90d93-116">-ResourceGroupName</span></span>
<span data-ttu-id="90d93-117">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="90d93-117">Resource Group Name</span></span>

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

### <span data-ttu-id="90d93-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="90d93-118">-Slot</span></span>
<span data-ttu-id="90d93-119">Nome do slot</span><span class="sxs-lookup"><span data-stu-id="90d93-119">Slot name</span></span>

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

### <span data-ttu-id="90d93-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="90d93-120">-WebApp</span></span>
<span data-ttu-id="90d93-121">WebApp canalizado</span><span class="sxs-lookup"><span data-stu-id="90d93-121">Piped WebApp</span></span>

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

### <span data-ttu-id="90d93-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90d93-122">CommonParameters</span></span>
<span data-ttu-id="90d93-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90d93-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90d93-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90d93-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90d93-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="90d93-125">INPUTS</span></span>

### <span data-ttu-id="90d93-126">System. String</span><span class="sxs-lookup"><span data-stu-id="90d93-126">System.String</span></span>

### <span data-ttu-id="90d93-127">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="90d93-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="90d93-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="90d93-128">OUTPUTS</span></span>

### <span data-ttu-id="90d93-129">Microsoft. Azure. Commands. webapps. cmdlets. webapps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="90d93-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="90d93-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="90d93-130">NOTES</span></span>

## <span data-ttu-id="90d93-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="90d93-131">RELATED LINKS</span></span>
