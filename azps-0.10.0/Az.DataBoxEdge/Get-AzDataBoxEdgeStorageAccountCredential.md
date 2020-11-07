---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: 4bc1e887ba1f5fc9918c6b01858cf9bd2c116ca6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776784"
---
# <span data-ttu-id="1eaa6-101">Get-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="1eaa6-101">Get-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="1eaa6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1eaa6-102">SYNOPSIS</span></span>
<span data-ttu-id="1eaa6-103">Obtém as credenciais da conta de armazenamento correspondentes à conta de armazenamento no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1eaa6-103">Gets the storage account credentials corresponding to the storage account on the device.</span></span>

## <span data-ttu-id="1eaa6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1eaa6-104">SYNTAX</span></span>

### <span data-ttu-id="1eaa6-105">ListParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="1eaa6-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1eaa6-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1eaa6-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1eaa6-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1eaa6-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1eaa6-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1eaa6-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="1eaa6-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1eaa6-109">DESCRIPTION</span></span>
<span data-ttu-id="1eaa6-110">O cmdlet **Get-AzDataBoxEdgeStorageAccountCredential** Obtém as credenciais da conta de armazenamento da conta de armazenamento correspondente no dispositivo de borda da caixa de dados.</span><span class="sxs-lookup"><span data-stu-id="1eaa6-110">The **Get-AzDataBoxEdgeStorageAccountCredential** cmdlet gets the storage account credentials for the corresponding storage account on the Data Box Edge device.</span></span> <span data-ttu-id="1eaa6-111">Você pode especificar o nome, o nome do grupo de recursos e os parâmetros do nome do dispositivo para obter informações sobre uma credencial específica da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1eaa6-111">You can specify Name, Resource Group Name and Device Name parameters to get information about a specific storage account credential.</span></span>

## <span data-ttu-id="1eaa6-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1eaa6-112">EXAMPLES</span></span>

### <span data-ttu-id="1eaa6-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1eaa6-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                          StorageAccount          SslStatus  ResourceGroupName
----------------------------- ---------------------- ---------- ---------------------
storageAccountCredentialName  StorageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="1eaa6-114">OS</span><span class="sxs-lookup"><span data-stu-id="1eaa6-114">PARAMETERS</span></span>

### <span data-ttu-id="1eaa6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1eaa6-115">-DefaultProfile</span></span>
<span data-ttu-id="1eaa6-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1eaa6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1eaa6-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="1eaa6-117">-DeviceName</span></span>
<span data-ttu-id="1eaa6-118">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="1eaa6-118">Device Name</span></span>

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

### <span data-ttu-id="1eaa6-119">-Deviceobject</span><span class="sxs-lookup"><span data-stu-id="1eaa6-119">-DeviceObject</span></span>
<span data-ttu-id="1eaa6-120">Forneça o objeto do dispositivo correspondente.</span><span class="sxs-lookup"><span data-stu-id="1eaa6-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="1eaa6-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="1eaa6-121">-Name</span></span>
<span data-ttu-id="1eaa6-122">Nome da conta de armazenamento a ser usada</span><span class="sxs-lookup"><span data-stu-id="1eaa6-122">Name of the storage account to be used</span></span>

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

### <span data-ttu-id="1eaa6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1eaa6-123">-ResourceGroupName</span></span>
<span data-ttu-id="1eaa6-124">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="1eaa6-124">Resource Group Name</span></span>

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

### <span data-ttu-id="1eaa6-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1eaa6-125">-ResourceId</span></span>
<span data-ttu-id="1eaa6-126">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="1eaa6-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="1eaa6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1eaa6-127">CommonParameters</span></span>
<span data-ttu-id="1eaa6-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1eaa6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1eaa6-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1eaa6-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1eaa6-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1eaa6-130">INPUTS</span></span>

### <span data-ttu-id="1eaa6-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="1eaa6-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="1eaa6-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1eaa6-132">OUTPUTS</span></span>

### <span data-ttu-id="1eaa6-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="1eaa6-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="1eaa6-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1eaa6-134">NOTES</span></span>

## <span data-ttu-id="1eaa6-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1eaa6-135">RELATED LINKS</span></span>
