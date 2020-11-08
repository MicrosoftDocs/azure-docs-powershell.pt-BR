---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeUser.md
ms.openlocfilehash: 3a9945d94b1aec3e82d4d79d09df0bacb3b3a11d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111276"
---
# <span data-ttu-id="e4308-101">Get-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="e4308-101">Get-AzStackEdgeUser</span></span>

## <span data-ttu-id="e4308-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e4308-102">SYNOPSIS</span></span>
<span data-ttu-id="e4308-103">Obtém os usuários configurados para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e4308-103">Gets the configured users for a device.</span></span>

## <span data-ttu-id="e4308-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e4308-104">SYNTAX</span></span>

### <span data-ttu-id="e4308-105">ListParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="e4308-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4308-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4308-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeUser -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4308-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4308-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4308-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4308-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeUser [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="e4308-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e4308-109">DESCRIPTION</span></span>
<span data-ttu-id="e4308-110">O cmdlet **Get-AzStackEdgeUser** lista os usuários configurados para um dispositivo de borda de pilha.</span><span class="sxs-lookup"><span data-stu-id="e4308-110">The **Get-AzStackEdgeUser** cmdlet lists the users configured for a Stack Edge device.</span></span> <span data-ttu-id="e4308-111">Você pode mencionar o nome nos parâmetros para obter detalhes sobre um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="e4308-111">You can mention the Name in parameters to get details about a specific user.</span></span>

## <span data-ttu-id="e4308-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e4308-112">EXAMPLES</span></span>

### <span data-ttu-id="e4308-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e4308-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName
User name  Type  ResourceGroupName DeviceName
---------  ----  ----------------- ----------
deviceName Share resourceGroupName deviceName
```

## <span data-ttu-id="e4308-114">OS</span><span class="sxs-lookup"><span data-stu-id="e4308-114">PARAMETERS</span></span>

### <span data-ttu-id="e4308-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4308-115">-DefaultProfile</span></span>
<span data-ttu-id="e4308-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e4308-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4308-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="e4308-117">-DeviceName</span></span>
<span data-ttu-id="e4308-118">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="e4308-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4308-119">-Deviceobject</span><span class="sxs-lookup"><span data-stu-id="e4308-119">-DeviceObject</span></span>
<span data-ttu-id="e4308-120">Forneça o objeto do dispositivo correspondente.</span><span class="sxs-lookup"><span data-stu-id="e4308-120">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4308-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="e4308-121">-Name</span></span>
<span data-ttu-id="e4308-122">Nome de usuário</span><span class="sxs-lookup"><span data-stu-id="e4308-122">Username</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: Username

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: Username

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4308-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4308-123">-ResourceGroupName</span></span>
<span data-ttu-id="e4308-124">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="e4308-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4308-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4308-125">-ResourceId</span></span>
<span data-ttu-id="e4308-126">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="e4308-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4308-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4308-127">CommonParameters</span></span>
<span data-ttu-id="e4308-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4308-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4308-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e4308-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4308-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e4308-130">INPUTS</span></span>

### <span data-ttu-id="e4308-131">Microsoft. Azure. PowerShell. cmdlets. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="e4308-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="e4308-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e4308-132">OUTPUTS</span></span>

### <span data-ttu-id="e4308-133">Microsoft. Azure. PowerShell. cmdlets. StackEdge. Models. PSStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="e4308-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="e4308-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e4308-134">NOTES</span></span>

## <span data-ttu-id="e4308-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e4308-135">RELATED LINKS</span></span>
