---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmDeletedWebApp.md
ms.openlocfilehash: 75ad4e1fabb511ee4ca3cff024389a8e826aeadd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430791"
---
# <span data-ttu-id="21577-101">Get-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="21577-101">Get-AzureRmDeletedWebApp</span></span>

## <span data-ttu-id="21577-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="21577-102">SYNOPSIS</span></span>
<span data-ttu-id="21577-103">Obtém aplicativos Web excluídos na assinatura.</span><span class="sxs-lookup"><span data-stu-id="21577-103">Gets deleted web apps in the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21577-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="21577-104">SYNTAX</span></span>

```
Get-AzureRmDeletedWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21577-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="21577-105">DESCRIPTION</span></span>
<span data-ttu-id="21577-106">O cmdlet **Get-AzureRmDeletedWebApp** retorna todos os aplicativos Web excluídos na assinatura.</span><span class="sxs-lookup"><span data-stu-id="21577-106">The **Get-AzureRmDeletedWebApp** cmdlet returns all deleted web apps in the subscription.</span></span> <span data-ttu-id="21577-107">Aplicativos excluídos podem ser filtrados opcionalmente por grupo de recursos, nome e slot.</span><span class="sxs-lookup"><span data-stu-id="21577-107">Deleted apps can optionally be filtered by resource group, name, and slot.</span></span> <span data-ttu-id="21577-108">Pode haver mais de um aplicativo excluído com o mesmo nome e grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="21577-108">There can be more than one deleted app with the same name and resource group.</span></span> <span data-ttu-id="21577-109">Marque a exclusão para distinguir os aplicativos excluídos que compartilham o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="21577-109">Check the DeletionTime to distinguish deleted apps that share the same name.</span></span>

## <span data-ttu-id="21577-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="21577-110">EXAMPLES</span></span>

### <span data-ttu-id="21577-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="21577-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeletedWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="21577-112">Esse comando obtém os aplicativos excluídos chamados ContosoSite pertencentes ao grupo de recursos padrão-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="21577-112">This command gets the deleted apps named ContosoSite belonging to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="21577-113">OS</span><span class="sxs-lookup"><span data-stu-id="21577-113">PARAMETERS</span></span>

### <span data-ttu-id="21577-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21577-114">-DefaultProfile</span></span>
<span data-ttu-id="21577-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="21577-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21577-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="21577-116">-Name</span></span>
<span data-ttu-id="21577-117">O nome do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="21577-117">The name of the web app.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21577-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21577-118">-ResourceGroupName</span></span>
<span data-ttu-id="21577-119">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="21577-119">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21577-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="21577-120">-Slot</span></span>
<span data-ttu-id="21577-121">O nome do slot do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="21577-121">The name of the web app slot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21577-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21577-122">CommonParameters</span></span>
<span data-ttu-id="21577-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21577-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="21577-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21577-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21577-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="21577-125">INPUTS</span></span>

### <span data-ttu-id="21577-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="21577-126">None</span></span>

## <span data-ttu-id="21577-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="21577-127">OUTPUTS</span></span>

### <span data-ttu-id="21577-128">Microsoft. Azure. Commands. webapps. cmdlets. webapps. PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="21577-128">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="21577-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="21577-129">NOTES</span></span>

## <span data-ttu-id="21577-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="21577-130">RELATED LINKS</span></span>

[<span data-ttu-id="21577-131">Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="21577-131">Restore-AzureRmDeletedWebApp</span></span>](./Restore-AzureRmDeletedWebApp.md)
