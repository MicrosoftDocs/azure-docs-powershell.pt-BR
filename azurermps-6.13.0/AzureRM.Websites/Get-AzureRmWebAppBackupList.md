---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappbackuplist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupList.md
ms.openlocfilehash: f4005df31746b63b2a45fa2c78f254e2d5f24c59
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427086"
---
# <span data-ttu-id="147a3-101">Get-AzureRmWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="147a3-101">Get-AzureRmWebAppBackupList</span></span>

## <span data-ttu-id="147a3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="147a3-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="147a3-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="147a3-103">SYNTAX</span></span>

### <span data-ttu-id="147a3-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="147a3-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="147a3-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="147a3-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackupList [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="147a3-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="147a3-106">DESCRIPTION</span></span>
<span data-ttu-id="147a3-107">O cmdlet **Get-AzureRmWebAppBackupList** Obtém uma lista de backups para um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="147a3-107">The **Get-AzureRmWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="147a3-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="147a3-108">EXAMPLES</span></span>

### <span data-ttu-id="147a3-109">1:</span><span class="sxs-lookup"><span data-stu-id="147a3-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="147a3-110">Esse comando retorna uma lista de backup relacionada a WebApp WebAppStandard associada à ContosoResourceGroup do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="147a3-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="147a3-111">OS</span><span class="sxs-lookup"><span data-stu-id="147a3-111">PARAMETERS</span></span>

### <span data-ttu-id="147a3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="147a3-112">-DefaultProfile</span></span>
<span data-ttu-id="147a3-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="147a3-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="147a3-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="147a3-114">-Name</span></span>
<span data-ttu-id="147a3-115">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="147a3-115">WebApp Name</span></span>

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

### <span data-ttu-id="147a3-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="147a3-116">-ResourceGroupName</span></span>
<span data-ttu-id="147a3-117">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="147a3-117">Resource Group Name</span></span>

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

### <span data-ttu-id="147a3-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="147a3-118">-Slot</span></span>
<span data-ttu-id="147a3-119">Nome do slot</span><span class="sxs-lookup"><span data-stu-id="147a3-119">Slot name</span></span>

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

### <span data-ttu-id="147a3-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="147a3-120">-WebApp</span></span>
<span data-ttu-id="147a3-121">WebApp canalizado</span><span class="sxs-lookup"><span data-stu-id="147a3-121">Piped WebApp</span></span>

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

### <span data-ttu-id="147a3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="147a3-122">CommonParameters</span></span>
<span data-ttu-id="147a3-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="147a3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="147a3-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="147a3-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="147a3-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="147a3-125">INPUTS</span></span>

### <span data-ttu-id="147a3-126">System. String</span><span class="sxs-lookup"><span data-stu-id="147a3-126">System.String</span></span>

### <span data-ttu-id="147a3-127">Microsoft. Azure. Management. WebSites. Models. site</span><span class="sxs-lookup"><span data-stu-id="147a3-127">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="147a3-128">Parâmetros: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="147a3-128">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="147a3-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="147a3-129">OUTPUTS</span></span>

### <span data-ttu-id="147a3-130">Microsoft. Azure. Commands. webapps. cmdlets. webapps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="147a3-130">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="147a3-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="147a3-131">NOTES</span></span>

## <span data-ttu-id="147a3-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="147a3-132">RELATED LINKS</span></span>
