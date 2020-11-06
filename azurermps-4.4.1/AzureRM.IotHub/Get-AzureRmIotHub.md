---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHub.md
ms.openlocfilehash: 890180c024a004652406e04530a7e3291def13ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441044"
---
# <span data-ttu-id="eb378-101">Get-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="eb378-101">Get-AzureRmIotHub</span></span>

## <span data-ttu-id="eb378-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eb378-102">SYNOPSIS</span></span>
<span data-ttu-id="eb378-103">Obtém informações sobre o IotHubs em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="eb378-103">Gets information about the IotHubs in a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb378-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eb378-104">SYNTAX</span></span>

### <span data-ttu-id="eb378-105">ListIotHubsByResourceGroup (padrão)</span><span class="sxs-lookup"><span data-stu-id="eb378-105">ListIotHubsByResourceGroup (Default)</span></span>
```
Get-AzureRmIotHub [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="eb378-106">GetIotHubByName</span><span class="sxs-lookup"><span data-stu-id="eb378-106">GetIotHubByName</span></span>
```
Get-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eb378-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="eb378-107">DESCRIPTION</span></span>
<span data-ttu-id="eb378-108">Obtém informações sobre o IotHubs em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="eb378-108">Gets information about the IotHubs in a subscription.</span></span>
<span data-ttu-id="eb378-109">Você pode exibir todas as instâncias de IotHub em uma assinatura ou filtrar seus resultados por um grupo de recursos ou um nome de IotHub específico.</span><span class="sxs-lookup"><span data-stu-id="eb378-109">You can view all IotHub instances in a subscription, or filter your results by a resource group or a particular IotHub Name.</span></span>

## <span data-ttu-id="eb378-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eb378-110">EXAMPLES</span></span>

### <span data-ttu-id="eb378-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="eb378-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIotHub
```

<span data-ttu-id="eb378-112">Obtém todas as IotHubs na assinatura.</span><span class="sxs-lookup"><span data-stu-id="eb378-112">Gets all the IotHubs in the subscription.</span></span>

### <span data-ttu-id="eb378-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="eb378-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIotHub -ResourceGroupName "myresourcegroup"
```

<span data-ttu-id="eb378-114">Obtém todos os IotHubs na assinatura pertencente ao The Resource, chamado "myresourceus".</span><span class="sxs-lookup"><span data-stu-id="eb378-114">Gets all the IotHubs in the subscription belonging to the resourcegroup named "myresourcegroup".</span></span>

### <span data-ttu-id="eb378-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="eb378-115">Example 3</span></span>
```
PS C:\> Get-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="eb378-116">Obtém informações sobre o IotHub chamado "myiothub".</span><span class="sxs-lookup"><span data-stu-id="eb378-116">Gets information about the IotHub named "myiothub".</span></span>

## <span data-ttu-id="eb378-117">OS</span><span class="sxs-lookup"><span data-stu-id="eb378-117">PARAMETERS</span></span>

### <span data-ttu-id="eb378-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="eb378-118">-Name</span></span>
<span data-ttu-id="eb378-119">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="eb378-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="eb378-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb378-120">-ResourceGroupName</span></span>
<span data-ttu-id="eb378-121">Nome do The Resource</span><span class="sxs-lookup"><span data-stu-id="eb378-121">Name of the ResourceGroup</span></span>

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

### <span data-ttu-id="eb378-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb378-122">-DefaultProfile</span></span>
<span data-ttu-id="eb378-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="eb378-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb378-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb378-124">CommonParameters</span></span>
<span data-ttu-id="eb378-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb378-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb378-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb378-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb378-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="eb378-127">INPUTS</span></span>

### <span data-ttu-id="eb378-128">System. String</span><span class="sxs-lookup"><span data-stu-id="eb378-128">System.String</span></span>

## <span data-ttu-id="eb378-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="eb378-129">OUTPUTS</span></span>

### <span data-ttu-id="eb378-130">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="eb378-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="eb378-131">System. Collections. Generic. List \` 1 \[ \[ Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="eb378-131">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="eb378-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="eb378-132">NOTES</span></span>

## <span data-ttu-id="eb378-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eb378-133">RELATED LINKS</span></span>

