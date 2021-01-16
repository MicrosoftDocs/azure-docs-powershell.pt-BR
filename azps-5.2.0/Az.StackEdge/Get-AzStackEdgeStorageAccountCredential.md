---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: f198db6a49e1f5165dcfcd4effd91106cc0df831
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263757"
---
# <span data-ttu-id="095db-101">Get-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="095db-101">Get-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="095db-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="095db-102">SYNOPSIS</span></span>
<span data-ttu-id="095db-103">Obtém as credenciais da conta de armazenamento correspondentes à conta de armazenamento no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="095db-103">Gets the storage account credentials corresponding to the storage account on the device.</span></span>

## <span data-ttu-id="095db-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="095db-104">SYNTAX</span></span>

### <span data-ttu-id="095db-105">ListParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="095db-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="095db-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="095db-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageAccountCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="095db-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="095db-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="095db-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="095db-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageAccountCredential [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="095db-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="095db-109">DESCRIPTION</span></span>
<span data-ttu-id="095db-110">O cmdlet **Get-AzStackEdgeStorageAccountCredential** Obtém as credenciais da conta de armazenamento da conta de armazenamento correspondente no dispositivo de borda de pilha.</span><span class="sxs-lookup"><span data-stu-id="095db-110">The **Get-AzStackEdgeStorageAccountCredential** cmdlet gets the storage account credentials for the corresponding storage account on the Stack Edge device.</span></span> <span data-ttu-id="095db-111">Você pode especificar o nome, o nome do grupo de recursos e os parâmetros do nome do dispositivo para obter informações sobre uma credencial específica da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="095db-111">You can specify Name, Resource Group Name and Device Name parameters to get information about a specific storage account credential.</span></span>

## <span data-ttu-id="095db-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="095db-112">EXAMPLES</span></span>

### <span data-ttu-id="095db-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="095db-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                          StorageAccount          SslStatus  ResourceGroupName
----------------------------- ---------------------- ---------- ---------------------
storageAccountCredentialName  StorageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="095db-114">OS</span><span class="sxs-lookup"><span data-stu-id="095db-114">PARAMETERS</span></span>

### <span data-ttu-id="095db-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="095db-115">-DefaultProfile</span></span>
<span data-ttu-id="095db-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="095db-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="095db-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="095db-117">-DeviceName</span></span>
<span data-ttu-id="095db-118">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="095db-118">Device Name</span></span>

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

### <span data-ttu-id="095db-119">-Deviceobject</span><span class="sxs-lookup"><span data-stu-id="095db-119">-DeviceObject</span></span>
<span data-ttu-id="095db-120">Forneça o objeto do dispositivo correspondente.</span><span class="sxs-lookup"><span data-stu-id="095db-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="095db-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="095db-121">-Name</span></span>
<span data-ttu-id="095db-122">Nome da conta de armazenamento a ser usada</span><span class="sxs-lookup"><span data-stu-id="095db-122">Name of the storage account to be used</span></span>

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

### <span data-ttu-id="095db-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="095db-123">-ResourceGroupName</span></span>
<span data-ttu-id="095db-124">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="095db-124">Resource Group Name</span></span>

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

### <span data-ttu-id="095db-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="095db-125">-ResourceId</span></span>
<span data-ttu-id="095db-126">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="095db-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="095db-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="095db-127">CommonParameters</span></span>
<span data-ttu-id="095db-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="095db-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="095db-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="095db-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="095db-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="095db-130">INPUTS</span></span>

### <span data-ttu-id="095db-131">Microsoft. Azure. PowerShell. cmdlets. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="095db-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="095db-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="095db-132">OUTPUTS</span></span>

### <span data-ttu-id="095db-133">Microsoft. Azure. PowerShell. cmdlets. StackEdge. Models. PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="095db-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="095db-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="095db-134">NOTES</span></span>

## <span data-ttu-id="095db-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="095db-135">RELATED LINKS</span></span>
