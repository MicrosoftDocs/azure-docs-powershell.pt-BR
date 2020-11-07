---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: EAAF615B-6139-438B-A2FD-6966E72B3AA9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappbackup
schema: 2.0.0
ms.openlocfilehash: c6d5809211910987e06cff024d7510a70ad71a4e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785133"
---
# <span data-ttu-id="f5f4c-101">Get-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="f5f4c-101">Get-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="f5f4c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f5f4c-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5f4c-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f5f4c-103">SYNTAX</span></span>

### <span data-ttu-id="f5f4c-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="f5f4c-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5f4c-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="f5f4c-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackup [-BackupId] <String> [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f5f4c-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f5f4c-106">DESCRIPTION</span></span>
<span data-ttu-id="f5f4c-107">O cmdlet **Get-AzureRmWebAppBackup** Obtém o backup especificado de um Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="f5f4c-107">The **Get-AzureRmWebAppBackup** cmdlet gets the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="f5f4c-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f5f4c-108">EXAMPLES</span></span>

### <span data-ttu-id="f5f4c-109">1:</span><span class="sxs-lookup"><span data-stu-id="f5f4c-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="f5f4c-110">Esse comando obtém o backup com ID "12345" do aplicativo Web chamado WebAppStandard que pertence ao grupo de recursos Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="f5f4c-110">This command gets the backup with ID "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="f5f4c-111">OS</span><span class="sxs-lookup"><span data-stu-id="f5f4c-111">PARAMETERS</span></span>

### <span data-ttu-id="f5f4c-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="f5f4c-112">-BackupId</span></span>
<span data-ttu-id="f5f4c-113">ID de backup</span><span class="sxs-lookup"><span data-stu-id="f5f4c-113">Backup Id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5f4c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5f4c-114">-DefaultProfile</span></span>
<span data-ttu-id="f5f4c-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f5f4c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5f4c-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="f5f4c-116">-Name</span></span>
<span data-ttu-id="f5f4c-117">Nome do webapp</span><span class="sxs-lookup"><span data-stu-id="f5f4c-117">Webapp Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5f4c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5f4c-118">-ResourceGroupName</span></span>
<span data-ttu-id="f5f4c-119">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f5f4c-119">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5f4c-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="f5f4c-120">-Slot</span></span>
<span data-ttu-id="f5f4c-121">Nome do slot</span><span class="sxs-lookup"><span data-stu-id="f5f4c-121">Slot Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5f4c-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="f5f4c-122">-WebApp</span></span>
<span data-ttu-id="f5f4c-123">WebApp canalizado</span><span class="sxs-lookup"><span data-stu-id="f5f4c-123">Piped WebApp</span></span>

```yaml
Type: Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5f4c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5f4c-124">CommonParameters</span></span>
<span data-ttu-id="f5f4c-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5f4c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5f4c-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5f4c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5f4c-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f5f4c-127">INPUTS</span></span>

### <span data-ttu-id="f5f4c-128">Instalação</span><span class="sxs-lookup"><span data-stu-id="f5f4c-128">Site</span></span>
<span data-ttu-id="f5f4c-129">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="f5f4c-129">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="f5f4c-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f5f4c-130">OUTPUTS</span></span>

### <span data-ttu-id="f5f4c-131">Microsoft. Azure. Commands. webapps. cmdlets. webapps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="f5f4c-131">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="f5f4c-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f5f4c-132">NOTES</span></span>

## <span data-ttu-id="f5f4c-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f5f4c-133">RELATED LINKS</span></span>

