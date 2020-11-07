---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 8337BEA9-4927-4718-83B9-F3F567BE0FBD
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppBackupConfiguration.md
ms.openlocfilehash: 4c6dc810d35feedd0d0d43e0bd3b3efb7c9b6641
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776119"
---
# <span data-ttu-id="82a81-101">Get-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="82a81-101">Get-AzWebAppBackupConfiguration</span></span>

## <span data-ttu-id="82a81-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="82a81-102">SYNOPSIS</span></span>

## <span data-ttu-id="82a81-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="82a81-103">SYNTAX</span></span>

### <span data-ttu-id="82a81-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="82a81-104">FromResourceName</span></span>
```
Get-AzWebAppBackupConfiguration [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82a81-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="82a81-105">FromWebApp</span></span>
```
Get-AzWebAppBackupConfiguration [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="82a81-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="82a81-106">DESCRIPTION</span></span>
<span data-ttu-id="82a81-107">O cmdlet **Get-AzWebAppBackupConfiguration** Obtém a configuração de backup de um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="82a81-107">The **Get-AzWebAppBackupConfiguration** cmdlet gets the backup configuration of an Azure Web App.</span></span>

## <span data-ttu-id="82a81-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="82a81-108">EXAMPLES</span></span>

### <span data-ttu-id="82a81-109">1:</span><span class="sxs-lookup"><span data-stu-id="82a81-109">1:</span></span>
```
PS C:\>Get-AzWebAppBackupConfiguration -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="82a81-110">Esse comando obtém a configuração de backup do aplicativo Web chamado WebAppStandard que pertence ao grupo de recursos Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="82a81-110">This command gets the backup configuration from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="82a81-111">OS</span><span class="sxs-lookup"><span data-stu-id="82a81-111">PARAMETERS</span></span>

### <span data-ttu-id="82a81-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82a81-112">-DefaultProfile</span></span>
<span data-ttu-id="82a81-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="82a81-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82a81-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="82a81-114">-Name</span></span>
<span data-ttu-id="82a81-115">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="82a81-115">WebApp Name</span></span>

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

### <span data-ttu-id="82a81-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82a81-116">-ResourceGroupName</span></span>
<span data-ttu-id="82a81-117">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="82a81-117">Resource Group Name</span></span>

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

### <span data-ttu-id="82a81-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="82a81-118">-Slot</span></span>
<span data-ttu-id="82a81-119">Nome do slot</span><span class="sxs-lookup"><span data-stu-id="82a81-119">Slot Name</span></span>

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

### <span data-ttu-id="82a81-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="82a81-120">-WebApp</span></span>
<span data-ttu-id="82a81-121">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="82a81-121">WebApp Name</span></span>

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

### <span data-ttu-id="82a81-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82a81-122">CommonParameters</span></span>
<span data-ttu-id="82a81-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82a81-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82a81-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82a81-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82a81-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="82a81-125">INPUTS</span></span>

### <span data-ttu-id="82a81-126">Instalação</span><span class="sxs-lookup"><span data-stu-id="82a81-126">Site</span></span>
<span data-ttu-id="82a81-127">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="82a81-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="82a81-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="82a81-128">OUTPUTS</span></span>

### <span data-ttu-id="82a81-129">Microsoft. Azure. Commands. webapps. cmdlets. webapps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="82a81-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="82a81-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="82a81-130">NOTES</span></span>

## <span data-ttu-id="82a81-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="82a81-131">RELATED LINKS</span></span>

