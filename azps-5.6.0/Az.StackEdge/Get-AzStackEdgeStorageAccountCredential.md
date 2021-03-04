---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/get-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: efb9c7828417596afecc21fc5e5c2b2b8f7c81b8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892598"
---
# <span data-ttu-id="980c5-101">Get-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="980c5-101">Get-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="980c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="980c5-102">SYNOPSIS</span></span>
<span data-ttu-id="980c5-103">Obtém as credenciais da conta de armazenamento correspondentes à conta de armazenamento no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="980c5-103">Gets the storage account credentials corresponding to the storage account on the device.</span></span>

## <span data-ttu-id="980c5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="980c5-104">SYNTAX</span></span>

### <span data-ttu-id="980c5-105">ListParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="980c5-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="980c5-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="980c5-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageAccountCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="980c5-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="980c5-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="980c5-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="980c5-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageAccountCredential [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="980c5-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="980c5-109">DESCRIPTION</span></span>
<span data-ttu-id="980c5-110">O cmdlet **Get-AzStackEdgeStorageAccountCredential** obtém as credenciais da conta de armazenamento para a conta de armazenamento correspondente no dispositivo de Borda de Pilha.</span><span class="sxs-lookup"><span data-stu-id="980c5-110">The **Get-AzStackEdgeStorageAccountCredential** cmdlet gets the storage account credentials for the corresponding storage account on the Stack Edge device.</span></span> <span data-ttu-id="980c5-111">Você pode especificar parâmetros Name, Resource Group Name e Device Name para obter informações sobre uma credencial de conta de armazenamento específica.</span><span class="sxs-lookup"><span data-stu-id="980c5-111">You can specify Name, Resource Group Name and Device Name parameters to get information about a specific storage account credential.</span></span>

## <span data-ttu-id="980c5-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="980c5-112">EXAMPLES</span></span>

### <span data-ttu-id="980c5-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="980c5-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                          StorageAccount          SslStatus  ResourceGroupName
----------------------------- ---------------------- ---------- ---------------------
storageAccountCredentialName  StorageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="980c5-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="980c5-114">PARAMETERS</span></span>

### <span data-ttu-id="980c5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="980c5-115">-DefaultProfile</span></span>
<span data-ttu-id="980c5-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="980c5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="980c5-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="980c5-117">-DeviceName</span></span>
<span data-ttu-id="980c5-118">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="980c5-118">Device Name</span></span>

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

### <span data-ttu-id="980c5-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="980c5-119">-DeviceObject</span></span>
<span data-ttu-id="980c5-120">Forneça o objeto de dispositivo correspondente</span><span class="sxs-lookup"><span data-stu-id="980c5-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="980c5-121">-Name</span><span class="sxs-lookup"><span data-stu-id="980c5-121">-Name</span></span>
<span data-ttu-id="980c5-122">Nome da conta de armazenamento a ser usada</span><span class="sxs-lookup"><span data-stu-id="980c5-122">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: StorageAccountCredentialName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: StorageAccountCredentialName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="980c5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="980c5-123">-ResourceGroupName</span></span>
<span data-ttu-id="980c5-124">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="980c5-124">Resource Group Name</span></span>

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

### <span data-ttu-id="980c5-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="980c5-125">-ResourceId</span></span>
<span data-ttu-id="980c5-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="980c5-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="980c5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="980c5-127">CommonParameters</span></span>
<span data-ttu-id="980c5-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="980c5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="980c5-129">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="980c5-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="980c5-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="980c5-130">INPUTS</span></span>

### <span data-ttu-id="980c5-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="980c5-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="980c5-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="980c5-132">OUTPUTS</span></span>

### <span data-ttu-id="980c5-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="980c5-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="980c5-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="980c5-134">NOTES</span></span>

## <span data-ttu-id="980c5-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="980c5-135">RELATED LINKS</span></span>
