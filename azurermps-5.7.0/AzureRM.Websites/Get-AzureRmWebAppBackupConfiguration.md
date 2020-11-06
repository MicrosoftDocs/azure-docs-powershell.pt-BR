---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 8337BEA9-4927-4718-83B9-F3F567BE0FBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupConfiguration.md
ms.openlocfilehash: 895b020753d1f4191b87430b14e2b843a4524eaa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426536"
---
# <span data-ttu-id="77c9f-101">Get-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="77c9f-101">Get-AzureRmWebAppBackupConfiguration</span></span>

## <span data-ttu-id="77c9f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="77c9f-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77c9f-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="77c9f-103">SYNTAX</span></span>

### <span data-ttu-id="77c9f-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="77c9f-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackupConfiguration [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77c9f-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="77c9f-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackupConfiguration [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="77c9f-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="77c9f-106">DESCRIPTION</span></span>
<span data-ttu-id="77c9f-107">O cmdlet **Get-AzureRmWebAppBackupConfiguration** Obtém a configuração de backup de um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="77c9f-107">The **Get-AzureRmWebAppBackupConfiguration** cmdlet gets the backup configuration of an Azure Web App.</span></span>

## <span data-ttu-id="77c9f-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="77c9f-108">EXAMPLES</span></span>

### <span data-ttu-id="77c9f-109">1:</span><span class="sxs-lookup"><span data-stu-id="77c9f-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackupConfiguration -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="77c9f-110">Esse comando obtém a configuração de backup do aplicativo Web chamado WebAppStandard que pertence ao grupo de recursos Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="77c9f-110">This command gets the backup configuration from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="77c9f-111">OS</span><span class="sxs-lookup"><span data-stu-id="77c9f-111">PARAMETERS</span></span>

### <span data-ttu-id="77c9f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77c9f-112">-DefaultProfile</span></span>
<span data-ttu-id="77c9f-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="77c9f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77c9f-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="77c9f-114">-Name</span></span>
<span data-ttu-id="77c9f-115">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="77c9f-115">WebApp Name</span></span>

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

### <span data-ttu-id="77c9f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77c9f-116">-ResourceGroupName</span></span>
<span data-ttu-id="77c9f-117">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="77c9f-117">Resource Group Name</span></span>

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

### <span data-ttu-id="77c9f-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="77c9f-118">-Slot</span></span>
<span data-ttu-id="77c9f-119">Nome do slot</span><span class="sxs-lookup"><span data-stu-id="77c9f-119">Slot Name</span></span>

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

### <span data-ttu-id="77c9f-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="77c9f-120">-WebApp</span></span>
<span data-ttu-id="77c9f-121">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="77c9f-121">WebApp Name</span></span>

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

### <span data-ttu-id="77c9f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77c9f-122">CommonParameters</span></span>
<span data-ttu-id="77c9f-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77c9f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77c9f-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77c9f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77c9f-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="77c9f-125">INPUTS</span></span>

### <span data-ttu-id="77c9f-126">Instalação</span><span class="sxs-lookup"><span data-stu-id="77c9f-126">Site</span></span>
<span data-ttu-id="77c9f-127">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="77c9f-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="77c9f-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="77c9f-128">OUTPUTS</span></span>

### <span data-ttu-id="77c9f-129">Microsoft. Azure. Commands. webapps. cmdlets. webapps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="77c9f-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="77c9f-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="77c9f-130">NOTES</span></span>

## <span data-ttu-id="77c9f-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="77c9f-131">RELATED LINKS</span></span>

