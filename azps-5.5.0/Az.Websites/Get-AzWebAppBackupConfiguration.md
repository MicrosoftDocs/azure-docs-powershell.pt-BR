---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 8337BEA9-4927-4718-83B9-F3F567BE0FBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupConfiguration.md
ms.openlocfilehash: 8ef8639c2ff79a326a8d0ffcdf1f1dca24dbccf9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118854"
---
# <span data-ttu-id="65984-101">Get-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="65984-101">Get-AzWebAppBackupConfiguration</span></span>

## <span data-ttu-id="65984-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="65984-102">SYNOPSIS</span></span>

## <span data-ttu-id="65984-103">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="65984-103">SYNTAX</span></span>

### <span data-ttu-id="65984-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="65984-104">FromResourceName</span></span>
```
Get-AzWebAppBackupConfiguration [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65984-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="65984-105">FromWebApp</span></span>
```
Get-AzWebAppBackupConfiguration [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="65984-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="65984-106">DESCRIPTION</span></span>
<span data-ttu-id="65984-107">O cmdlet **Get-AzWebAppBackupConfiguration** obtém a configuração de backup de um Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="65984-107">The **Get-AzWebAppBackupConfiguration** cmdlet gets the backup configuration of an Azure Web App.</span></span>

## <span data-ttu-id="65984-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="65984-108">EXAMPLES</span></span>

### <span data-ttu-id="65984-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="65984-109">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppBackupConfiguration -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="65984-110">Esse comando obtém a configuração de backup do Web App chamada WebAppStandard que pertence ao grupo de recursos Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="65984-110">This command gets the backup configuration from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="65984-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="65984-111">PARAMETERS</span></span>

### <span data-ttu-id="65984-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65984-112">-DefaultProfile</span></span>
<span data-ttu-id="65984-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="65984-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65984-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="65984-114">-Name</span></span>
<span data-ttu-id="65984-115">Nome webapp</span><span class="sxs-lookup"><span data-stu-id="65984-115">WebApp Name</span></span>

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

### <span data-ttu-id="65984-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65984-116">-ResourceGroupName</span></span>
<span data-ttu-id="65984-117">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="65984-117">Resource Group Name</span></span>

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

### <span data-ttu-id="65984-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="65984-118">-Slot</span></span>
<span data-ttu-id="65984-119">Nome do Slot</span><span class="sxs-lookup"><span data-stu-id="65984-119">Slot Name</span></span>

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

### <span data-ttu-id="65984-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="65984-120">-WebApp</span></span>
<span data-ttu-id="65984-121">Nome webapp</span><span class="sxs-lookup"><span data-stu-id="65984-121">WebApp Name</span></span>

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

### <span data-ttu-id="65984-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65984-122">CommonParameters</span></span>
<span data-ttu-id="65984-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65984-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65984-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65984-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65984-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="65984-125">INPUTS</span></span>

### <span data-ttu-id="65984-126">System.String</span><span class="sxs-lookup"><span data-stu-id="65984-126">System.String</span></span>

### <span data-ttu-id="65984-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="65984-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="65984-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="65984-128">OUTPUTS</span></span>

### <span data-ttu-id="65984-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="65984-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="65984-130">Notas</span><span class="sxs-lookup"><span data-stu-id="65984-130">NOTES</span></span>

## <span data-ttu-id="65984-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="65984-131">RELATED LINKS</span></span>
