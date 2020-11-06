---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 65A78654-A490-4B60-8C16-B0CC597EE995
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppBackup.md
ms.openlocfilehash: 98ded2967c364955ab8b9dd38f316021649d0fc8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429273"
---
# <span data-ttu-id="00703-101">Remove-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="00703-101">Remove-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="00703-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="00703-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00703-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="00703-103">SYNTAX</span></span>

### <span data-ttu-id="00703-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="00703-104">FromResourceName</span></span>
```
Remove-AzureRmWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00703-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="00703-105">FromWebApp</span></span>
```
Remove-AzureRmWebAppBackup [-BackupId] <String> [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="00703-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="00703-106">DESCRIPTION</span></span>
<span data-ttu-id="00703-107">O cmdlet **Remove-AzureRmWebAppBackup** remove o backup especificado de um Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="00703-107">The **Remove-AzureRmWebAppBackup** cmdlet removes the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="00703-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="00703-108">EXAMPLES</span></span>

### <span data-ttu-id="00703-109">1:</span><span class="sxs-lookup"><span data-stu-id="00703-109">1:</span></span>
```
PS C:\>Remove-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="00703-110">Esse comando Remove o backup com o ID de "12345" do aplicativo Web chamado WebAppStandard que pertence ao grupo de recursos padrão-Oesteus da Web.</span><span class="sxs-lookup"><span data-stu-id="00703-110">This command removes the backup with backup with ID of "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="00703-111">OS</span><span class="sxs-lookup"><span data-stu-id="00703-111">PARAMETERS</span></span>

### <span data-ttu-id="00703-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="00703-112">-BackupId</span></span>
<span data-ttu-id="00703-113">ID de backup</span><span class="sxs-lookup"><span data-stu-id="00703-113">Backup Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00703-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00703-114">-DefaultProfile</span></span>
<span data-ttu-id="00703-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="00703-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00703-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="00703-116">-Name</span></span>
<span data-ttu-id="00703-117">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="00703-117">WebApp Name</span></span>

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

### <span data-ttu-id="00703-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00703-118">-ResourceGroupName</span></span>
<span data-ttu-id="00703-119">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="00703-119">Resource Group Name</span></span>

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

### <span data-ttu-id="00703-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="00703-120">-Slot</span></span>
<span data-ttu-id="00703-121">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="00703-121">WebApp Slot Name</span></span>

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

### <span data-ttu-id="00703-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="00703-122">-WebApp</span></span>
<span data-ttu-id="00703-123">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="00703-123">WebApp Object</span></span>

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

### <span data-ttu-id="00703-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00703-124">CommonParameters</span></span>
<span data-ttu-id="00703-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00703-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00703-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00703-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00703-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="00703-127">INPUTS</span></span>

### <span data-ttu-id="00703-128">System. String</span><span class="sxs-lookup"><span data-stu-id="00703-128">System.String</span></span>

### <span data-ttu-id="00703-129">Microsoft. Azure. Management. WebSites. Models. site</span><span class="sxs-lookup"><span data-stu-id="00703-129">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="00703-130">Parâmetros: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="00703-130">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="00703-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="00703-131">OUTPUTS</span></span>

### <span data-ttu-id="00703-132">Microsoft. Azure. Management. WebSites. Models. BackupItem</span><span class="sxs-lookup"><span data-stu-id="00703-132">Microsoft.Azure.Management.WebSites.Models.BackupItem</span></span>

## <span data-ttu-id="00703-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="00703-133">NOTES</span></span>

## <span data-ttu-id="00703-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="00703-134">RELATED LINKS</span></span>
