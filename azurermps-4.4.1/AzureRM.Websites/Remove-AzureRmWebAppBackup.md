---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 65A78654-A490-4B60-8C16-B0CC597EE995
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppBackup.md
ms.openlocfilehash: ba7255c41b5851b1f34b2ff7a1523c691925bae0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440913"
---
# <span data-ttu-id="f0484-101">Remove-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="f0484-101">Remove-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="f0484-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f0484-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0484-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f0484-103">SYNTAX</span></span>

### <span data-ttu-id="f0484-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="f0484-104">FromResourceName</span></span>
```
Remove-AzureRmWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0484-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="f0484-105">FromWebApp</span></span>
```
Remove-AzureRmWebAppBackup [-BackupId] <String> [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f0484-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f0484-106">DESCRIPTION</span></span>
<span data-ttu-id="f0484-107">O cmdlet **Remove-AzureRmWebAppBackup** remove o backup especificado de um Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="f0484-107">The **Remove-AzureRmWebAppBackup** cmdlet removes the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="f0484-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f0484-108">EXAMPLES</span></span>

### <span data-ttu-id="f0484-109">1:</span><span class="sxs-lookup"><span data-stu-id="f0484-109">1:</span></span>
```
PS C:\>Remove-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="f0484-110">Esse comando Remove o backup com o ID de "12345" do aplicativo Web chamado WebAppStandard que pertence ao grupo de recursos padrão-Oesteus da Web.</span><span class="sxs-lookup"><span data-stu-id="f0484-110">This command removes the backup with backup with ID of "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="f0484-111">OS</span><span class="sxs-lookup"><span data-stu-id="f0484-111">PARAMETERS</span></span>

### <span data-ttu-id="f0484-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="f0484-112">-BackupId</span></span>
<span data-ttu-id="f0484-113">ID de backup</span><span class="sxs-lookup"><span data-stu-id="f0484-113">Backup Id</span></span>

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

### <span data-ttu-id="f0484-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="f0484-114">-Name</span></span>
<span data-ttu-id="f0484-115">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="f0484-115">WebApp Name</span></span>

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

### <span data-ttu-id="f0484-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0484-116">-ResourceGroupName</span></span>
<span data-ttu-id="f0484-117">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f0484-117">Resource Group Name</span></span>

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

### <span data-ttu-id="f0484-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="f0484-118">-Slot</span></span>
<span data-ttu-id="f0484-119">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="f0484-119">WebApp Slot Name</span></span>

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

### <span data-ttu-id="f0484-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="f0484-120">-WebApp</span></span>
<span data-ttu-id="f0484-121">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="f0484-121">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0484-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0484-122">-DefaultProfile</span></span>
<span data-ttu-id="f0484-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f0484-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0484-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0484-124">CommonParameters</span></span>
<span data-ttu-id="f0484-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0484-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0484-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0484-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0484-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f0484-127">INPUTS</span></span>

### <span data-ttu-id="f0484-128">Instalação</span><span class="sxs-lookup"><span data-stu-id="f0484-128">Site</span></span>
<span data-ttu-id="f0484-129">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="f0484-129">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="f0484-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f0484-130">OUTPUTS</span></span>

### <span data-ttu-id="f0484-131">Microsoft. Azure. Management. WebSites. Models. BackupItem</span><span class="sxs-lookup"><span data-stu-id="f0484-131">Microsoft.Azure.Management.WebSites.Models.BackupItem</span></span>

## <span data-ttu-id="f0484-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f0484-132">NOTES</span></span>

## <span data-ttu-id="f0484-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f0484-133">RELATED LINKS</span></span>

