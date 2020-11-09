---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 8337BEA9-4927-4718-83B9-F3F567BE0FBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupConfiguration.md
ms.openlocfilehash: 8ef8639c2ff79a326a8d0ffcdf1f1dca24dbccf9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281792"
---
# <span data-ttu-id="5ac4a-101">Get-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="5ac4a-101">Get-AzWebAppBackupConfiguration</span></span>

## <span data-ttu-id="5ac4a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5ac4a-102">SYNOPSIS</span></span>

## <span data-ttu-id="5ac4a-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5ac4a-103">SYNTAX</span></span>

### <span data-ttu-id="5ac4a-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="5ac4a-104">FromResourceName</span></span>
```
Get-AzWebAppBackupConfiguration [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ac4a-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="5ac4a-105">FromWebApp</span></span>
```
Get-AzWebAppBackupConfiguration [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5ac4a-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5ac4a-106">DESCRIPTION</span></span>
<span data-ttu-id="5ac4a-107">O cmdlet **Get-AzWebAppBackupConfiguration** Obtém a configuração de backup de um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="5ac4a-107">The **Get-AzWebAppBackupConfiguration** cmdlet gets the backup configuration of an Azure Web App.</span></span>

## <span data-ttu-id="5ac4a-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5ac4a-108">EXAMPLES</span></span>

### <span data-ttu-id="5ac4a-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5ac4a-109">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppBackupConfiguration -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="5ac4a-110">Esse comando obtém a configuração de backup do aplicativo Web chamado WebAppStandard que pertence ao grupo de recursos Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="5ac4a-110">This command gets the backup configuration from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="5ac4a-111">OS</span><span class="sxs-lookup"><span data-stu-id="5ac4a-111">PARAMETERS</span></span>

### <span data-ttu-id="5ac4a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ac4a-112">-DefaultProfile</span></span>
<span data-ttu-id="5ac4a-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5ac4a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ac4a-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="5ac4a-114">-Name</span></span>
<span data-ttu-id="5ac4a-115">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="5ac4a-115">WebApp Name</span></span>

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

### <span data-ttu-id="5ac4a-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ac4a-116">-ResourceGroupName</span></span>
<span data-ttu-id="5ac4a-117">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="5ac4a-117">Resource Group Name</span></span>

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

### <span data-ttu-id="5ac4a-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="5ac4a-118">-Slot</span></span>
<span data-ttu-id="5ac4a-119">Nome do slot</span><span class="sxs-lookup"><span data-stu-id="5ac4a-119">Slot Name</span></span>

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

### <span data-ttu-id="5ac4a-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="5ac4a-120">-WebApp</span></span>
<span data-ttu-id="5ac4a-121">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="5ac4a-121">WebApp Name</span></span>

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

### <span data-ttu-id="5ac4a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ac4a-122">CommonParameters</span></span>
<span data-ttu-id="5ac4a-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ac4a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ac4a-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ac4a-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ac4a-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5ac4a-125">INPUTS</span></span>

### <span data-ttu-id="5ac4a-126">System. String</span><span class="sxs-lookup"><span data-stu-id="5ac4a-126">System.String</span></span>

### <span data-ttu-id="5ac4a-127">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="5ac4a-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="5ac4a-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5ac4a-128">OUTPUTS</span></span>

### <span data-ttu-id="5ac4a-129">Microsoft. Azure. Commands. webapps. cmdlets. webapps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="5ac4a-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="5ac4a-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5ac4a-130">NOTES</span></span>

## <span data-ttu-id="5ac4a-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5ac4a-131">RELATED LINKS</span></span>
