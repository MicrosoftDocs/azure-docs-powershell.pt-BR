---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EAAF615B-6139-438B-A2FD-6966E72B3AA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackup.md
ms.openlocfilehash: e8c3f7543062613527e7f52be2cd6493f53c5f60
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112018"
---
# <span data-ttu-id="5585e-101">Get-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="5585e-101">Get-AzWebAppBackup</span></span>

## <span data-ttu-id="5585e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5585e-102">SYNOPSIS</span></span>

## <span data-ttu-id="5585e-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5585e-103">SYNTAX</span></span>

### <span data-ttu-id="5585e-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="5585e-104">FromResourceName</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5585e-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="5585e-105">FromWebApp</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5585e-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5585e-106">DESCRIPTION</span></span>
<span data-ttu-id="5585e-107">O cmdlet **Get-AzWebAppBackup** Obtém o backup especificado de um Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="5585e-107">The **Get-AzWebAppBackup** cmdlet gets the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="5585e-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5585e-108">EXAMPLES</span></span>

### <span data-ttu-id="5585e-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5585e-109">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="5585e-110">Esse comando obtém o backup com ID "12345" do aplicativo Web chamado WebAppStandard que pertence ao grupo de recursos Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="5585e-110">This command gets the backup with ID "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="5585e-111">OS</span><span class="sxs-lookup"><span data-stu-id="5585e-111">PARAMETERS</span></span>

### <span data-ttu-id="5585e-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="5585e-112">-BackupId</span></span>
<span data-ttu-id="5585e-113">ID de backup</span><span class="sxs-lookup"><span data-stu-id="5585e-113">Backup Id</span></span>

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

### <span data-ttu-id="5585e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5585e-114">-DefaultProfile</span></span>
<span data-ttu-id="5585e-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5585e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5585e-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="5585e-116">-Name</span></span>
<span data-ttu-id="5585e-117">Nome do webapp</span><span class="sxs-lookup"><span data-stu-id="5585e-117">Webapp Name</span></span>

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

### <span data-ttu-id="5585e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5585e-118">-ResourceGroupName</span></span>
<span data-ttu-id="5585e-119">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="5585e-119">Resource Group Name</span></span>

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

### <span data-ttu-id="5585e-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="5585e-120">-Slot</span></span>
<span data-ttu-id="5585e-121">Nome do slot</span><span class="sxs-lookup"><span data-stu-id="5585e-121">Slot Name</span></span>

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

### <span data-ttu-id="5585e-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="5585e-122">-WebApp</span></span>
<span data-ttu-id="5585e-123">WebApp canalizado</span><span class="sxs-lookup"><span data-stu-id="5585e-123">Piped WebApp</span></span>

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

### <span data-ttu-id="5585e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5585e-124">CommonParameters</span></span>
<span data-ttu-id="5585e-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5585e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5585e-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5585e-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5585e-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5585e-127">INPUTS</span></span>

### <span data-ttu-id="5585e-128">System. String</span><span class="sxs-lookup"><span data-stu-id="5585e-128">System.String</span></span>

### <span data-ttu-id="5585e-129">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="5585e-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="5585e-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5585e-130">OUTPUTS</span></span>

### <span data-ttu-id="5585e-131">Microsoft. Azure. Commands. webapps. cmdlets. webapps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="5585e-131">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="5585e-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5585e-132">NOTES</span></span>

## <span data-ttu-id="5585e-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5585e-133">RELATED LINKS</span></span>
