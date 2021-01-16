---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHub.md
ms.openlocfilehash: 0656726757584bf923d6ecaa7642aa67ff46596a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260501"
---
# <span data-ttu-id="76d71-101">Get-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="76d71-101">Get-AzIotHub</span></span>

## <span data-ttu-id="76d71-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="76d71-102">SYNOPSIS</span></span>
<span data-ttu-id="76d71-103">Obtém informações sobre o IotHubs em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="76d71-103">Gets information about the IotHubs in a subscription.</span></span>

## <span data-ttu-id="76d71-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="76d71-104">SYNTAX</span></span>

### <span data-ttu-id="76d71-105">ListIotHubsByResourceGroup (padrão)</span><span class="sxs-lookup"><span data-stu-id="76d71-105">ListIotHubsByResourceGroup (Default)</span></span>
```
Get-AzIotHub [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76d71-106">GetIotHubByName</span><span class="sxs-lookup"><span data-stu-id="76d71-106">GetIotHubByName</span></span>
```
Get-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="76d71-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="76d71-107">DESCRIPTION</span></span>
<span data-ttu-id="76d71-108">Obtém informações sobre o IotHubs em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="76d71-108">Gets information about the IotHubs in a subscription.</span></span>
<span data-ttu-id="76d71-109">Você pode exibir todas as instâncias de IotHub em uma assinatura ou filtrar seus resultados por um grupo de recursos ou um nome de IotHub específico.</span><span class="sxs-lookup"><span data-stu-id="76d71-109">You can view all IotHub instances in a subscription, or filter your results by a resource group or a particular IotHub Name.</span></span>

## <span data-ttu-id="76d71-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="76d71-110">EXAMPLES</span></span>

### <span data-ttu-id="76d71-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="76d71-111">Example 1</span></span>
```
PS C:\> Get-AzIotHub
```

<span data-ttu-id="76d71-112">Obtém todas as IotHubs na assinatura.</span><span class="sxs-lookup"><span data-stu-id="76d71-112">Gets all the IotHubs in the subscription.</span></span>

### <span data-ttu-id="76d71-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="76d71-113">Example 2</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup"
```

<span data-ttu-id="76d71-114">Obtém todos os IotHubs na assinatura pertencente ao The Resource, chamado "myresourceus".</span><span class="sxs-lookup"><span data-stu-id="76d71-114">Gets all the IotHubs in the subscription belonging to the resourcegroup named "myresourcegroup".</span></span>

### <span data-ttu-id="76d71-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="76d71-115">Example 3</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="76d71-116">Obtém informações sobre o IotHub chamado "myiothub".</span><span class="sxs-lookup"><span data-stu-id="76d71-116">Gets information about the IotHub named "myiothub".</span></span>

## <span data-ttu-id="76d71-117">OS</span><span class="sxs-lookup"><span data-stu-id="76d71-117">PARAMETERS</span></span>

### <span data-ttu-id="76d71-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76d71-118">-DefaultProfile</span></span>
<span data-ttu-id="76d71-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="76d71-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="76d71-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="76d71-120">-Name</span></span>
<span data-ttu-id="76d71-121">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="76d71-121">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: GetIotHubByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76d71-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76d71-122">-ResourceGroupName</span></span>
<span data-ttu-id="76d71-123">Nome do The Resource</span><span class="sxs-lookup"><span data-stu-id="76d71-123">Name of the ResourceGroup</span></span>

```yaml
Type: System.String
Parameter Sets: ListIotHubsByResourceGroup
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetIotHubByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76d71-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76d71-124">CommonParameters</span></span>
<span data-ttu-id="76d71-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76d71-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76d71-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76d71-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76d71-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="76d71-127">INPUTS</span></span>

### <span data-ttu-id="76d71-128">System. String</span><span class="sxs-lookup"><span data-stu-id="76d71-128">System.String</span></span>

## <span data-ttu-id="76d71-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="76d71-129">OUTPUTS</span></span>

### <span data-ttu-id="76d71-130">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="76d71-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="76d71-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="76d71-131">NOTES</span></span>

## <span data-ttu-id="76d71-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="76d71-132">RELATED LINKS</span></span>
