---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
ms.openlocfilehash: 258d1e1bad9eca1fd8817e1eaa499eb5bc3d8d49
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262424"
---
# <span data-ttu-id="2f4a4-101">Get-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="2f4a4-101">Get-AzIotHubKey</span></span>

## <span data-ttu-id="2f4a4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2f4a4-102">SYNOPSIS</span></span>
<span data-ttu-id="2f4a4-103">Obtém uma chave IotHub.</span><span class="sxs-lookup"><span data-stu-id="2f4a4-103">Gets an IotHub Key.</span></span>

## <span data-ttu-id="2f4a4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2f4a4-104">SYNTAX</span></span>

### <span data-ttu-id="2f4a4-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="2f4a4-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f4a4-106">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="2f4a4-106">ResourceIdSet</span></span>
```
Get-AzIotHubKey [-HubId] <String> [[-KeyName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2f4a4-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2f4a4-107">DESCRIPTION</span></span>
<span data-ttu-id="2f4a4-108">Obtém uma chave IotHub.</span><span class="sxs-lookup"><span data-stu-id="2f4a4-108">Gets an IotHub Key.</span></span>
<span data-ttu-id="2f4a4-109">Você pode listar todas as chaves ou filtrar a lista por um nome de chave específico.</span><span class="sxs-lookup"><span data-stu-id="2f4a4-109">You can either list all Keys or filter the list by a specific Key Name.</span></span>

## <span data-ttu-id="2f4a4-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2f4a4-110">EXAMPLES</span></span>

### <span data-ttu-id="2f4a4-111">Exemplo 1 obter todas as chaves</span><span class="sxs-lookup"><span data-stu-id="2f4a4-111">Example 1 Get all Keys</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="2f4a4-112">Obtém todas as chaves para o IotHub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="2f4a4-112">Gets all the Keys for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="2f4a4-113">Exemplo 2 obter informações para uma tecla específica</span><span class="sxs-lookup"><span data-stu-id="2f4a4-113">Example 2 Get information for a specific Key</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner"
```

<span data-ttu-id="2f4a4-114">Obtém as informações de uma chave chamada "iothubowner" para o IotHub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="2f4a4-114">Gets the information for a key named "iothubowner" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="2f4a4-115">OS</span><span class="sxs-lookup"><span data-stu-id="2f4a4-115">PARAMETERS</span></span>

### <span data-ttu-id="2f4a4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f4a4-116">-DefaultProfile</span></span>
<span data-ttu-id="2f4a4-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="2f4a4-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2f4a4-118">-HubId</span><span class="sxs-lookup"><span data-stu-id="2f4a4-118">-HubId</span></span>
<span data-ttu-id="2f4a4-119">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="2f4a4-119">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f4a4-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="2f4a4-120">-KeyName</span></span>
<span data-ttu-id="2f4a4-121">Nome da chave</span><span class="sxs-lookup"><span data-stu-id="2f4a4-121">Name of the Key</span></span>

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

### <span data-ttu-id="2f4a4-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="2f4a4-122">-Name</span></span>
<span data-ttu-id="2f4a4-123">Nome do Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="2f4a4-123">Name of the IoT hub.</span></span> 

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f4a4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f4a4-124">-ResourceGroupName</span></span>
<span data-ttu-id="2f4a4-125">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="2f4a4-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f4a4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f4a4-126">CommonParameters</span></span>
<span data-ttu-id="2f4a4-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f4a4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f4a4-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f4a4-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f4a4-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2f4a4-129">INPUTS</span></span>

### <span data-ttu-id="2f4a4-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2f4a4-130">System.String</span></span>

## <span data-ttu-id="2f4a4-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2f4a4-131">OUTPUTS</span></span>

### <span data-ttu-id="2f4a4-132">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="2f4a4-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="2f4a4-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2f4a4-133">NOTES</span></span>

## <span data-ttu-id="2f4a4-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2f4a4-134">RELATED LINKS</span></span>
