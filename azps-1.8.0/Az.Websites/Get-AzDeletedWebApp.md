---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzDeletedWebApp.md
ms.openlocfilehash: fabbaf6e34a39767c9ca0acdadd3fdc05d8e260f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598368"
---
# <span data-ttu-id="b78cc-101">Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="b78cc-101">Get-AzDeletedWebApp</span></span>

## <span data-ttu-id="b78cc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b78cc-102">SYNOPSIS</span></span>
<span data-ttu-id="b78cc-103">Obtém aplicativos Web excluídos na assinatura.</span><span class="sxs-lookup"><span data-stu-id="b78cc-103">Gets deleted web apps in the subscription.</span></span>

## <span data-ttu-id="b78cc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b78cc-104">SYNTAX</span></span>

```
Get-AzDeletedWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b78cc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b78cc-105">DESCRIPTION</span></span>
<span data-ttu-id="b78cc-106">O cmdlet **Get-AzDeletedWebApp** retorna todos os aplicativos Web excluídos na assinatura.</span><span class="sxs-lookup"><span data-stu-id="b78cc-106">The **Get-AzDeletedWebApp** cmdlet returns all deleted web apps in the subscription.</span></span> <span data-ttu-id="b78cc-107">Aplicativos excluídos podem ser filtrados opcionalmente por grupo de recursos, nome e slot.</span><span class="sxs-lookup"><span data-stu-id="b78cc-107">Deleted apps can optionally be filtered by resource group, name, and slot.</span></span> <span data-ttu-id="b78cc-108">Pode haver mais de um aplicativo excluído com o mesmo nome e grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b78cc-108">There can be more than one deleted app with the same name and resource group.</span></span> <span data-ttu-id="b78cc-109">Marque a exclusão para distinguir os aplicativos excluídos que compartilham o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="b78cc-109">Check the DeletionTime to distinguish deleted apps that share the same name.</span></span>

## <span data-ttu-id="b78cc-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b78cc-110">EXAMPLES</span></span>

### <span data-ttu-id="b78cc-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b78cc-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeletedWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="b78cc-112">Esse comando obtém os aplicativos excluídos chamados ContosoSite pertencentes ao grupo de recursos padrão-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="b78cc-112">This command gets the deleted apps named ContosoSite belonging to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="b78cc-113">OS</span><span class="sxs-lookup"><span data-stu-id="b78cc-113">PARAMETERS</span></span>

### <span data-ttu-id="b78cc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b78cc-114">-DefaultProfile</span></span>
<span data-ttu-id="b78cc-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b78cc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b78cc-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="b78cc-116">-Name</span></span>
<span data-ttu-id="b78cc-117">O nome do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="b78cc-117">The name of the web app.</span></span>

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

### <span data-ttu-id="b78cc-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b78cc-118">-ResourceGroupName</span></span>
<span data-ttu-id="b78cc-119">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b78cc-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="b78cc-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="b78cc-120">-Slot</span></span>
<span data-ttu-id="b78cc-121">O nome do slot do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="b78cc-121">The name of the web app slot.</span></span>

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

### <span data-ttu-id="b78cc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b78cc-122">CommonParameters</span></span>
<span data-ttu-id="b78cc-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b78cc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b78cc-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b78cc-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b78cc-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b78cc-125">INPUTS</span></span>

### <span data-ttu-id="b78cc-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="b78cc-126">None</span></span>

## <span data-ttu-id="b78cc-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b78cc-127">OUTPUTS</span></span>

### <span data-ttu-id="b78cc-128">Microsoft. Azure. Commands. webapps. cmdlets. webapps. PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="b78cc-128">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="b78cc-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b78cc-129">NOTES</span></span>

## <span data-ttu-id="b78cc-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b78cc-130">RELATED LINKS</span></span>

[<span data-ttu-id="b78cc-131">Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="b78cc-131">Restore-AzDeletedWebApp</span></span>](./Restore-AzDeletedWebApp.md)