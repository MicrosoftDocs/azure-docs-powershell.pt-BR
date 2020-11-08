---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzDeletedWebApp.md
ms.openlocfilehash: 74c518d4713c19c7a1bb7b7d0b3341e164e22c35
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113131"
---
# <span data-ttu-id="d5c1c-101">Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="d5c1c-101">Get-AzDeletedWebApp</span></span>

## <span data-ttu-id="d5c1c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d5c1c-102">SYNOPSIS</span></span>
<span data-ttu-id="d5c1c-103">Obtém aplicativos Web excluídos na assinatura.</span><span class="sxs-lookup"><span data-stu-id="d5c1c-103">Gets deleted web apps in the subscription.</span></span>

## <span data-ttu-id="d5c1c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d5c1c-104">SYNTAX</span></span>

```
Get-AzDeletedWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [[-Slot] <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5c1c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d5c1c-105">DESCRIPTION</span></span>
<span data-ttu-id="d5c1c-106">O cmdlet **Get-AzDeletedWebApp** retorna todos os aplicativos Web excluídos na assinatura.</span><span class="sxs-lookup"><span data-stu-id="d5c1c-106">The **Get-AzDeletedWebApp** cmdlet returns all deleted web apps in the subscription.</span></span> <span data-ttu-id="d5c1c-107">Aplicativos excluídos podem ser filtrados opcionalmente por grupo de recursos, nome e slot.</span><span class="sxs-lookup"><span data-stu-id="d5c1c-107">Deleted apps can optionally be filtered by resource group, name, and slot.</span></span> <span data-ttu-id="d5c1c-108">Pode haver mais de um aplicativo excluído com o mesmo nome e grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d5c1c-108">There can be more than one deleted app with the same name and resource group.</span></span> <span data-ttu-id="d5c1c-109">Marque a exclusão para distinguir os aplicativos excluídos que compartilham o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="d5c1c-109">Check the DeletionTime to distinguish deleted apps that share the same name.</span></span>

## <span data-ttu-id="d5c1c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d5c1c-110">EXAMPLES</span></span>

### <span data-ttu-id="d5c1c-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d5c1c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeletedWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="d5c1c-112">Esse comando obtém os aplicativos excluídos chamados ContosoSite pertencentes ao grupo de recursos padrão-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="d5c1c-112">This command gets the deleted apps named ContosoSite belonging to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="d5c1c-113">OS</span><span class="sxs-lookup"><span data-stu-id="d5c1c-113">PARAMETERS</span></span>

### <span data-ttu-id="d5c1c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5c1c-114">-DefaultProfile</span></span>
<span data-ttu-id="d5c1c-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d5c1c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5c1c-116">-Local</span><span class="sxs-lookup"><span data-stu-id="d5c1c-116">-Location</span></span>
<span data-ttu-id="d5c1c-117">O local do aplicativo excluído.</span><span class="sxs-lookup"><span data-stu-id="d5c1c-117">The location of the deleted app.</span></span>

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

### <span data-ttu-id="d5c1c-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="d5c1c-118">-Name</span></span>
<span data-ttu-id="d5c1c-119">O nome do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="d5c1c-119">The name of the web app.</span></span>

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

### <span data-ttu-id="d5c1c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5c1c-120">-ResourceGroupName</span></span>
<span data-ttu-id="d5c1c-121">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d5c1c-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="d5c1c-122">-Slot</span><span class="sxs-lookup"><span data-stu-id="d5c1c-122">-Slot</span></span>
<span data-ttu-id="d5c1c-123">O nome do slot do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="d5c1c-123">The name of the web app slot.</span></span>

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

### <span data-ttu-id="d5c1c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5c1c-124">CommonParameters</span></span>
<span data-ttu-id="d5c1c-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5c1c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5c1c-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5c1c-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5c1c-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d5c1c-127">INPUTS</span></span>

### <span data-ttu-id="d5c1c-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d5c1c-128">None</span></span>

## <span data-ttu-id="d5c1c-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d5c1c-129">OUTPUTS</span></span>

### <span data-ttu-id="d5c1c-130">Microsoft. Azure. Commands. webapps. cmdlets. webapps. PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="d5c1c-130">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="d5c1c-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d5c1c-131">NOTES</span></span>

## <span data-ttu-id="d5c1c-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d5c1c-132">RELATED LINKS</span></span>

[<span data-ttu-id="d5c1c-133">Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="d5c1c-133">Restore-AzDeletedWebApp</span></span>](./Restore-AzDeletedWebApp.md)