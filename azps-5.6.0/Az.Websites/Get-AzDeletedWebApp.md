---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzDeletedWebApp.md
ms.openlocfilehash: a67e48cdcad9d80d244e74ef8e20f81fcbd157cd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889372"
---
# <span data-ttu-id="b8c44-101">Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="b8c44-101">Get-AzDeletedWebApp</span></span>

## <span data-ttu-id="b8c44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8c44-102">SYNOPSIS</span></span>
<span data-ttu-id="b8c44-103">Obtém aplicativos Web excluídos na assinatura.</span><span class="sxs-lookup"><span data-stu-id="b8c44-103">Gets deleted web apps in the subscription.</span></span>

## <span data-ttu-id="b8c44-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b8c44-104">SYNTAX</span></span>

```
Get-AzDeletedWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [[-Slot] <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8c44-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b8c44-105">DESCRIPTION</span></span>
<span data-ttu-id="b8c44-106">O cmdlet **Get-AzDeletedWebApp** retorna todos os aplicativos Web excluídos na assinatura.</span><span class="sxs-lookup"><span data-stu-id="b8c44-106">The **Get-AzDeletedWebApp** cmdlet returns all deleted web apps in the subscription.</span></span> <span data-ttu-id="b8c44-107">Os aplicativos excluídos podem, opcionalmente, ser filtrados por grupo de recursos, nome e slot.</span><span class="sxs-lookup"><span data-stu-id="b8c44-107">Deleted apps can optionally be filtered by resource group, name, and slot.</span></span> <span data-ttu-id="b8c44-108">Pode haver mais de um aplicativo excluído com o mesmo nome e grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b8c44-108">There can be more than one deleted app with the same name and resource group.</span></span> <span data-ttu-id="b8c44-109">Verifique o DeletionTime para distinguir aplicativos excluídos que compartilham o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="b8c44-109">Check the DeletionTime to distinguish deleted apps that share the same name.</span></span>

## <span data-ttu-id="b8c44-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b8c44-110">EXAMPLES</span></span>

### <span data-ttu-id="b8c44-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b8c44-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeletedWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="b8c44-112">Este comando obtém os aplicativos excluídos chamados ContosoSite pertencentes ao grupo de recursos Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="b8c44-112">This command gets the deleted apps named ContosoSite belonging to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="b8c44-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b8c44-113">PARAMETERS</span></span>

### <span data-ttu-id="b8c44-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8c44-114">-DefaultProfile</span></span>
<span data-ttu-id="b8c44-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b8c44-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8c44-116">-Location</span><span class="sxs-lookup"><span data-stu-id="b8c44-116">-Location</span></span>
<span data-ttu-id="b8c44-117">O local do aplicativo excluído.</span><span class="sxs-lookup"><span data-stu-id="b8c44-117">The location of the deleted app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8c44-118">-Name</span><span class="sxs-lookup"><span data-stu-id="b8c44-118">-Name</span></span>
<span data-ttu-id="b8c44-119">O nome do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="b8c44-119">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8c44-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8c44-120">-ResourceGroupName</span></span>
<span data-ttu-id="b8c44-121">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b8c44-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8c44-122">-Slot</span><span class="sxs-lookup"><span data-stu-id="b8c44-122">-Slot</span></span>
<span data-ttu-id="b8c44-123">O nome do slot do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="b8c44-123">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8c44-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8c44-124">CommonParameters</span></span>
<span data-ttu-id="b8c44-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8c44-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8c44-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8c44-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8c44-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b8c44-127">INPUTS</span></span>

### <span data-ttu-id="b8c44-128">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b8c44-128">None</span></span>

## <span data-ttu-id="b8c44-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b8c44-129">OUTPUTS</span></span>

### <span data-ttu-id="b8c44-130">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="b8c44-130">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="b8c44-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="b8c44-131">NOTES</span></span>

## <span data-ttu-id="b8c44-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b8c44-132">RELATED LINKS</span></span>

[<span data-ttu-id="b8c44-133">Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="b8c44-133">Restore-AzDeletedWebApp</span></span>](./Restore-AzDeletedWebApp.md)