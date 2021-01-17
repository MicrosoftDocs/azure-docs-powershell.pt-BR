---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 65A78654-A490-4B60-8C16-B0CC597EE995
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppBackup.md
ms.openlocfilehash: e50c711e730f3af79ce5d8825e6beeee9b663e00
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427792"
---
# <span data-ttu-id="5b3e2-101">Remove-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="5b3e2-101">Remove-AzWebAppBackup</span></span>

## <span data-ttu-id="5b3e2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5b3e2-102">SYNOPSIS</span></span>

## <span data-ttu-id="5b3e2-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5b3e2-103">SYNTAX</span></span>

### <span data-ttu-id="5b3e2-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="5b3e2-104">FromResourceName</span></span>
```
Remove-AzWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b3e2-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="5b3e2-105">FromWebApp</span></span>
```
Remove-AzWebAppBackup [-BackupId] <String> [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5b3e2-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5b3e2-106">DESCRIPTION</span></span>
<span data-ttu-id="5b3e2-107">O cmdlet **Remove-AzWebAppBackup** remove o backup especificado de um Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="5b3e2-107">The **Remove-AzWebAppBackup** cmdlet removes the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="5b3e2-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5b3e2-108">EXAMPLES</span></span>

### <span data-ttu-id="5b3e2-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5b3e2-109">Example 1</span></span>
```powershell
PS C:\>Remove-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="5b3e2-110">Esse comando Remove o backup com o ID de "12345" do aplicativo Web chamado WebAppStandard que pertence ao grupo de recursos padrão-Oesteus da Web.</span><span class="sxs-lookup"><span data-stu-id="5b3e2-110">This command removes the backup with backup with ID of "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="5b3e2-111">OS</span><span class="sxs-lookup"><span data-stu-id="5b3e2-111">PARAMETERS</span></span>

### <span data-ttu-id="5b3e2-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="5b3e2-112">-BackupId</span></span>
<span data-ttu-id="5b3e2-113">ID de backup</span><span class="sxs-lookup"><span data-stu-id="5b3e2-113">Backup Id</span></span>

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

### <span data-ttu-id="5b3e2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b3e2-114">-DefaultProfile</span></span>
<span data-ttu-id="5b3e2-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5b3e2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b3e2-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="5b3e2-116">-Name</span></span>
<span data-ttu-id="5b3e2-117">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="5b3e2-117">WebApp Name</span></span>

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

### <span data-ttu-id="5b3e2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b3e2-118">-ResourceGroupName</span></span>
<span data-ttu-id="5b3e2-119">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="5b3e2-119">Resource Group Name</span></span>

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

### <span data-ttu-id="5b3e2-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="5b3e2-120">-Slot</span></span>
<span data-ttu-id="5b3e2-121">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="5b3e2-121">WebApp Slot Name</span></span>

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

### <span data-ttu-id="5b3e2-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="5b3e2-122">-WebApp</span></span>
<span data-ttu-id="5b3e2-123">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="5b3e2-123">WebApp Object</span></span>

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

### <span data-ttu-id="5b3e2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b3e2-124">CommonParameters</span></span>
<span data-ttu-id="5b3e2-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b3e2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b3e2-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b3e2-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b3e2-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5b3e2-127">INPUTS</span></span>

### <span data-ttu-id="5b3e2-128">System. String</span><span class="sxs-lookup"><span data-stu-id="5b3e2-128">System.String</span></span>

### <span data-ttu-id="5b3e2-129">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="5b3e2-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="5b3e2-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5b3e2-130">OUTPUTS</span></span>

### <span data-ttu-id="5b3e2-131">Microsoft. Azure. Management. WebSites. Models. BackupItem</span><span class="sxs-lookup"><span data-stu-id="5b3e2-131">Microsoft.Azure.Management.WebSites.Models.BackupItem</span></span>

## <span data-ttu-id="5b3e2-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5b3e2-132">NOTES</span></span>

## <span data-ttu-id="5b3e2-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5b3e2-133">RELATED LINKS</span></span>
