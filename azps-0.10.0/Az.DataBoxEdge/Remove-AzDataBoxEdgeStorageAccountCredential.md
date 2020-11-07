---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: dff83dbb7183c4f9eaf46e883a92a8e615f9cacc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776745"
---
# <span data-ttu-id="a3e61-101">Remove-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="a3e61-101">Remove-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="a3e61-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a3e61-102">SYNOPSIS</span></span>
<span data-ttu-id="a3e61-103">Remove uma credencial de conta de armazenamento de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a3e61-103">Removes a storage account credential for a device.</span></span>

## <span data-ttu-id="a3e61-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a3e61-104">SYNTAX</span></span>

### <span data-ttu-id="a3e61-105">DeleteByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="a3e61-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a3e61-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3e61-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccountCredential [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3e61-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3e61-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccountCredential [-InputObject] <PSDataBoxEdgeStorageAccountCredential> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3e61-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a3e61-108">DESCRIPTION</span></span>
<span data-ttu-id="a3e61-109">O cmdlet **Remove-AzDataBoxEdgeStorageAccountCredential** remove a credencial da conta de armazenamento de um dispositivo de borda de caixa de dados.</span><span class="sxs-lookup"><span data-stu-id="a3e61-109">The **Remove-AzDataBoxEdgeStorageAccountCredential** cmdlet removes the storage account credential for a Data Box Edge device.</span></span>

## <span data-ttu-id="a3e61-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a3e61-110">EXAMPLES</span></span>

### <span data-ttu-id="a3e61-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a3e61-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeStorageAccountCredential ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAccountCredentialName
```

## <span data-ttu-id="a3e61-112">OS</span><span class="sxs-lookup"><span data-stu-id="a3e61-112">PARAMETERS</span></span>

### <span data-ttu-id="a3e61-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a3e61-113">-AsJob</span></span>
<span data-ttu-id="a3e61-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="a3e61-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3e61-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3e61-115">-DefaultProfile</span></span>
<span data-ttu-id="a3e61-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a3e61-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3e61-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="a3e61-117">-DeviceName</span></span>
<span data-ttu-id="a3e61-118">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="a3e61-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3e61-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3e61-119">-InputObject</span></span>
<span data-ttu-id="a3e61-120">Objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="a3e61-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3e61-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="a3e61-121">-Name</span></span>
<span data-ttu-id="a3e61-122">Nome da conta de armazenamento a ser usada</span><span class="sxs-lookup"><span data-stu-id="a3e61-122">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3e61-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a3e61-123">-PassThru</span></span>
<span data-ttu-id="a3e61-124">Retorna verdadeiro se bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="a3e61-124">returns true if successful</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3e61-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3e61-125">-ResourceGroupName</span></span>
<span data-ttu-id="a3e61-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="a3e61-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3e61-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3e61-127">-ResourceId</span></span>
<span data-ttu-id="a3e61-128">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="a3e61-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3e61-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a3e61-129">-Confirm</span></span>
<span data-ttu-id="a3e61-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3e61-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3e61-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3e61-131">-WhatIf</span></span>
<span data-ttu-id="a3e61-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a3e61-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a3e61-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a3e61-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3e61-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3e61-134">CommonParameters</span></span>
<span data-ttu-id="a3e61-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3e61-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3e61-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a3e61-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3e61-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a3e61-137">INPUTS</span></span>

### <span data-ttu-id="a3e61-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a3e61-138">System.String</span></span>

### <span data-ttu-id="a3e61-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="a3e61-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="a3e61-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a3e61-140">OUTPUTS</span></span>

### <span data-ttu-id="a3e61-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a3e61-141">System.Boolean</span></span>

## <span data-ttu-id="a3e61-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a3e61-142">NOTES</span></span>

## <span data-ttu-id="a3e61-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a3e61-143">RELATED LINKS</span></span>
