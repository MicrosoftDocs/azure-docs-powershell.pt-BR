---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappbackuplist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupList.md
ms.openlocfilehash: 6ea805f1e3a3711c2efe6faefd73edf06c4b51fd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116274"
---
# <span data-ttu-id="71ebd-101">Get-AzWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="71ebd-101">Get-AzWebAppBackupList</span></span>

## <span data-ttu-id="71ebd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="71ebd-102">SYNOPSIS</span></span>

## <span data-ttu-id="71ebd-103">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="71ebd-103">SYNTAX</span></span>

### <span data-ttu-id="71ebd-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="71ebd-104">FromResourceName</span></span>
```
Get-AzWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71ebd-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="71ebd-105">FromWebApp</span></span>
```
Get-AzWebAppBackupList [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71ebd-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="71ebd-106">DESCRIPTION</span></span>
<span data-ttu-id="71ebd-107">O cmdlet **Get-AzWebAppBackupList** obtém uma lista de backups para um Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="71ebd-107">The **Get-AzWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="71ebd-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="71ebd-108">EXAMPLES</span></span>

### <span data-ttu-id="71ebd-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="71ebd-109">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="71ebd-110">Esse comando retorna uma lista de backup referente ao WebApp WebAppStandard associada ao grupo de recursos ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="71ebd-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="71ebd-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="71ebd-111">PARAMETERS</span></span>

### <span data-ttu-id="71ebd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71ebd-112">-DefaultProfile</span></span>
<span data-ttu-id="71ebd-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="71ebd-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71ebd-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="71ebd-114">-Name</span></span>
<span data-ttu-id="71ebd-115">Nome webapp</span><span class="sxs-lookup"><span data-stu-id="71ebd-115">WebApp Name</span></span>

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

### <span data-ttu-id="71ebd-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71ebd-116">-ResourceGroupName</span></span>
<span data-ttu-id="71ebd-117">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="71ebd-117">Resource Group Name</span></span>

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

### <span data-ttu-id="71ebd-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="71ebd-118">-Slot</span></span>
<span data-ttu-id="71ebd-119">Nome do slot</span><span class="sxs-lookup"><span data-stu-id="71ebd-119">Slot name</span></span>

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

### <span data-ttu-id="71ebd-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="71ebd-120">-WebApp</span></span>
<span data-ttu-id="71ebd-121">WebApp encadeado</span><span class="sxs-lookup"><span data-stu-id="71ebd-121">Piped WebApp</span></span>

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

### <span data-ttu-id="71ebd-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71ebd-122">CommonParameters</span></span>
<span data-ttu-id="71ebd-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71ebd-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71ebd-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71ebd-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71ebd-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="71ebd-125">INPUTS</span></span>

### <span data-ttu-id="71ebd-126">System.String</span><span class="sxs-lookup"><span data-stu-id="71ebd-126">System.String</span></span>

### <span data-ttu-id="71ebd-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="71ebd-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="71ebd-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="71ebd-128">OUTPUTS</span></span>

### <span data-ttu-id="71ebd-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="71ebd-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="71ebd-130">Notas</span><span class="sxs-lookup"><span data-stu-id="71ebd-130">NOTES</span></span>

## <span data-ttu-id="71ebd-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="71ebd-131">RELATED LINKS</span></span>
