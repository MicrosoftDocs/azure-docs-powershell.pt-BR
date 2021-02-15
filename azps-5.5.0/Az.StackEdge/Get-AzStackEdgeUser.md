---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeUser.md
ms.openlocfilehash: 3a9945d94b1aec3e82d4d79d09df0bacb3b3a11d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112522"
---
# <span data-ttu-id="20c40-101">Get-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="20c40-101">Get-AzStackEdgeUser</span></span>

## <span data-ttu-id="20c40-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="20c40-102">SYNOPSIS</span></span>
<span data-ttu-id="20c40-103">Obtém os usuários configurados para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20c40-103">Gets the configured users for a device.</span></span>

## <span data-ttu-id="20c40-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="20c40-104">SYNTAX</span></span>

### <span data-ttu-id="20c40-105">ListParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="20c40-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20c40-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="20c40-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeUser -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20c40-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="20c40-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20c40-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="20c40-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeUser [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="20c40-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="20c40-109">DESCRIPTION</span></span>
<span data-ttu-id="20c40-110">O **cmdlet Get-AzSt stackEdgeUser** lista os usuários configurados para um dispositivo de Borda de Pilha.</span><span class="sxs-lookup"><span data-stu-id="20c40-110">The **Get-AzStackEdgeUser** cmdlet lists the users configured for a Stack Edge device.</span></span> <span data-ttu-id="20c40-111">Você pode mencionar o Nome nos parâmetros para obter detalhes sobre um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="20c40-111">You can mention the Name in parameters to get details about a specific user.</span></span>

## <span data-ttu-id="20c40-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="20c40-112">EXAMPLES</span></span>

### <span data-ttu-id="20c40-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="20c40-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName
User name  Type  ResourceGroupName DeviceName
---------  ----  ----------------- ----------
deviceName Share resourceGroupName deviceName
```

## <span data-ttu-id="20c40-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="20c40-114">PARAMETERS</span></span>

### <span data-ttu-id="20c40-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20c40-115">-DefaultProfile</span></span>
<span data-ttu-id="20c40-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="20c40-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20c40-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="20c40-117">-DeviceName</span></span>
<span data-ttu-id="20c40-118">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="20c40-118">Device Name</span></span>

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

### <span data-ttu-id="20c40-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="20c40-119">-DeviceObject</span></span>
<span data-ttu-id="20c40-120">Forneça o objeto do dispositivo correspondente</span><span class="sxs-lookup"><span data-stu-id="20c40-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="20c40-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="20c40-121">-Name</span></span>
<span data-ttu-id="20c40-122">Username</span><span class="sxs-lookup"><span data-stu-id="20c40-122">Username</span></span>

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

### <span data-ttu-id="20c40-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20c40-123">-ResourceGroupName</span></span>
<span data-ttu-id="20c40-124">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="20c40-124">Resource Group Name</span></span>

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

### <span data-ttu-id="20c40-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="20c40-125">-ResourceId</span></span>
<span data-ttu-id="20c40-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="20c40-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="20c40-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20c40-127">CommonParameters</span></span>
<span data-ttu-id="20c40-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20c40-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20c40-129">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="20c40-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20c40-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="20c40-130">INPUTS</span></span>

### <span data-ttu-id="20c40-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSSt stackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="20c40-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="20c40-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="20c40-132">OUTPUTS</span></span>

### <span data-ttu-id="20c40-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSSt stackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="20c40-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="20c40-134">Notas</span><span class="sxs-lookup"><span data-stu-id="20c40-134">NOTES</span></span>

## <span data-ttu-id="20c40-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="20c40-135">RELATED LINKS</span></span>
