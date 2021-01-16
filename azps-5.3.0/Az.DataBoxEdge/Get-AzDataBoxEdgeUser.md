---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeUser.md
ms.openlocfilehash: cc03472aa71665a8612e17bfce6365a255f929bd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433968"
---
# <span data-ttu-id="151a6-101">Get-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="151a6-101">Get-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="151a6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="151a6-102">SYNOPSIS</span></span>
<span data-ttu-id="151a6-103">Obtém os usuários configurados para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="151a6-103">Gets the configured users for a device.</span></span>

## <span data-ttu-id="151a6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="151a6-104">SYNTAX</span></span>

### <span data-ttu-id="151a6-105">ListParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="151a6-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="151a6-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="151a6-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeUser -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="151a6-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="151a6-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="151a6-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="151a6-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeUser [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="151a6-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="151a6-109">DESCRIPTION</span></span>
<span data-ttu-id="151a6-110">O cmdlet **Get-AzDataBoxEdgeUser** lista os usuários configurados para um dispositivo de borda de caixa de dados.</span><span class="sxs-lookup"><span data-stu-id="151a6-110">The **Get-AzDataBoxEdgeUser** cmdlet lists the users configured for a Data Box Edge device.</span></span> <span data-ttu-id="151a6-111">Você pode mencionar o nome nos parâmetros para obter detalhes sobre um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="151a6-111">You can mention the Name in parameters to get details about a specific user.</span></span>

## <span data-ttu-id="151a6-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="151a6-112">EXAMPLES</span></span>

### <span data-ttu-id="151a6-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="151a6-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName
User name  Type  ResourceGroupName DeviceName
---------  ----  ----------------- ----------
deviceName Share resourceGroupName deviceName
```

## <span data-ttu-id="151a6-114">OS</span><span class="sxs-lookup"><span data-stu-id="151a6-114">PARAMETERS</span></span>

### <span data-ttu-id="151a6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="151a6-115">-DefaultProfile</span></span>
<span data-ttu-id="151a6-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="151a6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="151a6-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="151a6-117">-DeviceName</span></span>
<span data-ttu-id="151a6-118">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="151a6-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="151a6-119">-Deviceobject</span><span class="sxs-lookup"><span data-stu-id="151a6-119">-DeviceObject</span></span>
<span data-ttu-id="151a6-120">Forneça o objeto do dispositivo correspondente.</span><span class="sxs-lookup"><span data-stu-id="151a6-120">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="151a6-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="151a6-121">-Name</span></span>
<span data-ttu-id="151a6-122">Nome de usuário</span><span class="sxs-lookup"><span data-stu-id="151a6-122">Username</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="151a6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="151a6-123">-ResourceGroupName</span></span>
<span data-ttu-id="151a6-124">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="151a6-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="151a6-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="151a6-125">-ResourceId</span></span>
<span data-ttu-id="151a6-126">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="151a6-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="151a6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="151a6-127">CommonParameters</span></span>
<span data-ttu-id="151a6-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="151a6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="151a6-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="151a6-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="151a6-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="151a6-130">INPUTS</span></span>

### <span data-ttu-id="151a6-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="151a6-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="151a6-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="151a6-132">OUTPUTS</span></span>

### <span data-ttu-id="151a6-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="151a6-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="151a6-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="151a6-134">NOTES</span></span>

## <span data-ttu-id="151a6-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="151a6-135">RELATED LINKS</span></span>
