---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 65A78654-A490-4B60-8C16-B0CC597EE995
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppBackup.md
ms.openlocfilehash: 508aa5245d56af85136ee475a420819d8224b491
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774444"
---
# <span data-ttu-id="f6900-101">Remove-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="f6900-101">Remove-AzWebAppBackup</span></span>

## <span data-ttu-id="f6900-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f6900-102">SYNOPSIS</span></span>

## <span data-ttu-id="f6900-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f6900-103">SYNTAX</span></span>

### <span data-ttu-id="f6900-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="f6900-104">FromResourceName</span></span>
```
Remove-AzWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6900-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="f6900-105">FromWebApp</span></span>
```
Remove-AzWebAppBackup [-BackupId] <String> [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f6900-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f6900-106">DESCRIPTION</span></span>
<span data-ttu-id="f6900-107">O cmdlet **Remove-AzWebAppBackup** remove o backup especificado de um Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="f6900-107">The **Remove-AzWebAppBackup** cmdlet removes the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="f6900-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f6900-108">EXAMPLES</span></span>

### <span data-ttu-id="f6900-109">1:</span><span class="sxs-lookup"><span data-stu-id="f6900-109">1:</span></span>
```
PS C:\>Remove-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="f6900-110">Esse comando Remove o backup com o ID de "12345" do aplicativo Web chamado WebAppStandard que pertence ao grupo de recursos padrão-Oesteus da Web.</span><span class="sxs-lookup"><span data-stu-id="f6900-110">This command removes the backup with backup with ID of "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="f6900-111">OS</span><span class="sxs-lookup"><span data-stu-id="f6900-111">PARAMETERS</span></span>

### <span data-ttu-id="f6900-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="f6900-112">-BackupId</span></span>
<span data-ttu-id="f6900-113">ID de backup</span><span class="sxs-lookup"><span data-stu-id="f6900-113">Backup Id</span></span>

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

### <span data-ttu-id="f6900-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6900-114">-DefaultProfile</span></span>
<span data-ttu-id="f6900-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f6900-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6900-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="f6900-116">-Name</span></span>
<span data-ttu-id="f6900-117">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="f6900-117">WebApp Name</span></span>

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

### <span data-ttu-id="f6900-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6900-118">-ResourceGroupName</span></span>
<span data-ttu-id="f6900-119">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f6900-119">Resource Group Name</span></span>

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

### <span data-ttu-id="f6900-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="f6900-120">-Slot</span></span>
<span data-ttu-id="f6900-121">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="f6900-121">WebApp Slot Name</span></span>

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

### <span data-ttu-id="f6900-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="f6900-122">-WebApp</span></span>
<span data-ttu-id="f6900-123">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="f6900-123">WebApp Object</span></span>

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

### <span data-ttu-id="f6900-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6900-124">CommonParameters</span></span>
<span data-ttu-id="f6900-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6900-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6900-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6900-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6900-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f6900-127">INPUTS</span></span>

### <span data-ttu-id="f6900-128">System. String</span><span class="sxs-lookup"><span data-stu-id="f6900-128">System.String</span></span>

### <span data-ttu-id="f6900-129">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="f6900-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="f6900-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f6900-130">OUTPUTS</span></span>

### <span data-ttu-id="f6900-131">Microsoft. Azure. Management. WebSites. Models. BackupItem</span><span class="sxs-lookup"><span data-stu-id="f6900-131">Microsoft.Azure.Management.WebSites.Models.BackupItem</span></span>

## <span data-ttu-id="f6900-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f6900-132">NOTES</span></span>

## <span data-ttu-id="f6900-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f6900-133">RELATED LINKS</span></span>
