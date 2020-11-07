---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHub.md
ms.openlocfilehash: d544de6badaa6ce64e8165696cc7dff2a595d75e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770733"
---
# <span data-ttu-id="91db8-101">Get-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="91db8-101">Get-AzIotHub</span></span>

## <span data-ttu-id="91db8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="91db8-102">SYNOPSIS</span></span>
<span data-ttu-id="91db8-103">Obtém informações sobre o IotHubs em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="91db8-103">Gets information about the IotHubs in a subscription.</span></span>

## <span data-ttu-id="91db8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="91db8-104">SYNTAX</span></span>

### <span data-ttu-id="91db8-105">ListIotHubsByResourceGroup (padrão)</span><span class="sxs-lookup"><span data-stu-id="91db8-105">ListIotHubsByResourceGroup (Default)</span></span>
```
Get-AzIotHub [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91db8-106">GetIotHubByName</span><span class="sxs-lookup"><span data-stu-id="91db8-106">GetIotHubByName</span></span>
```
Get-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="91db8-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="91db8-107">DESCRIPTION</span></span>
<span data-ttu-id="91db8-108">Obtém informações sobre o IotHubs em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="91db8-108">Gets information about the IotHubs in a subscription.</span></span>
<span data-ttu-id="91db8-109">Você pode exibir todas as instâncias de IotHub em uma assinatura ou filtrar seus resultados por um grupo de recursos ou um nome de IotHub específico.</span><span class="sxs-lookup"><span data-stu-id="91db8-109">You can view all IotHub instances in a subscription, or filter your results by a resource group or a particular IotHub Name.</span></span>

## <span data-ttu-id="91db8-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="91db8-110">EXAMPLES</span></span>

### <span data-ttu-id="91db8-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="91db8-111">Example 1</span></span>
```
PS C:\> Get-AzIotHub
```

<span data-ttu-id="91db8-112">Obtém todas as IotHubs na assinatura.</span><span class="sxs-lookup"><span data-stu-id="91db8-112">Gets all the IotHubs in the subscription.</span></span>

### <span data-ttu-id="91db8-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="91db8-113">Example 2</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup"
```

<span data-ttu-id="91db8-114">Obtém todos os IotHubs na assinatura pertencente ao The Resource, chamado "myresourceus".</span><span class="sxs-lookup"><span data-stu-id="91db8-114">Gets all the IotHubs in the subscription belonging to the resourcegroup named "myresourcegroup".</span></span>

### <span data-ttu-id="91db8-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="91db8-115">Example 3</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="91db8-116">Obtém informações sobre o IotHub chamado "myiothub".</span><span class="sxs-lookup"><span data-stu-id="91db8-116">Gets information about the IotHub named "myiothub".</span></span>

## <span data-ttu-id="91db8-117">OS</span><span class="sxs-lookup"><span data-stu-id="91db8-117">PARAMETERS</span></span>

### <span data-ttu-id="91db8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91db8-118">-DefaultProfile</span></span>
<span data-ttu-id="91db8-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="91db8-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="91db8-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="91db8-120">-Name</span></span>
<span data-ttu-id="91db8-121">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="91db8-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="91db8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91db8-122">-ResourceGroupName</span></span>
<span data-ttu-id="91db8-123">Nome do The Resource</span><span class="sxs-lookup"><span data-stu-id="91db8-123">Name of the ResourceGroup</span></span>

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

### <span data-ttu-id="91db8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91db8-124">CommonParameters</span></span>
<span data-ttu-id="91db8-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91db8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91db8-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91db8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91db8-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="91db8-127">INPUTS</span></span>

### <span data-ttu-id="91db8-128">System. String</span><span class="sxs-lookup"><span data-stu-id="91db8-128">System.String</span></span>

## <span data-ttu-id="91db8-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="91db8-129">OUTPUTS</span></span>

### <span data-ttu-id="91db8-130">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="91db8-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="91db8-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="91db8-131">NOTES</span></span>

## <span data-ttu-id="91db8-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="91db8-132">RELATED LINKS</span></span>
