---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: 1a55a8c08182ae4a32e27bec74e4a5870aae95fa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113211"
---
# <span data-ttu-id="4b817-101">Remove-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="4b817-101">Remove-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="4b817-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4b817-102">SYNOPSIS</span></span>
<span data-ttu-id="4b817-103">Remove uma credencial de conta de armazenamento de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4b817-103">Removes a storage account credential for a device.</span></span>

## <span data-ttu-id="4b817-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4b817-104">SYNTAX</span></span>

### <span data-ttu-id="4b817-105">DeleteByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="4b817-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4b817-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b817-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccountCredential [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b817-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b817-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccountCredential [-InputObject] <PSStackEdgeStorageAccountCredential> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b817-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4b817-108">DESCRIPTION</span></span>
<span data-ttu-id="4b817-109">O cmdlet **Remove-AzStackEdgeStorageAccountCredential** remove a credencial da conta de armazenamento de um dispositivo de borda de pilha.</span><span class="sxs-lookup"><span data-stu-id="4b817-109">The **Remove-AzStackEdgeStorageAccountCredential** cmdlet removes the storage account credential for a Stack Edge device.</span></span>

## <span data-ttu-id="4b817-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4b817-110">EXAMPLES</span></span>

### <span data-ttu-id="4b817-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4b817-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeStorageAccountCredential ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAccountCredentialName
```

## <span data-ttu-id="4b817-112">OS</span><span class="sxs-lookup"><span data-stu-id="4b817-112">PARAMETERS</span></span>

### <span data-ttu-id="4b817-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4b817-113">-AsJob</span></span>
<span data-ttu-id="4b817-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="4b817-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4b817-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b817-115">-DefaultProfile</span></span>
<span data-ttu-id="4b817-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4b817-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b817-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="4b817-117">-DeviceName</span></span>
<span data-ttu-id="4b817-118">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="4b817-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b817-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4b817-119">-InputObject</span></span>
<span data-ttu-id="4b817-120">Objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="4b817-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: StorageAccountCredential

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4b817-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="4b817-121">-Name</span></span>
<span data-ttu-id="4b817-122">Nome da conta de armazenamento a ser usada</span><span class="sxs-lookup"><span data-stu-id="4b817-122">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: StorageAccountCredentialName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b817-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4b817-123">-PassThru</span></span>
<span data-ttu-id="4b817-124">Retorna verdadeiro se bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="4b817-124">returns true if successful</span></span>

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

### <span data-ttu-id="4b817-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b817-125">-ResourceGroupName</span></span>
<span data-ttu-id="4b817-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="4b817-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b817-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4b817-127">-ResourceId</span></span>
<span data-ttu-id="4b817-128">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="4b817-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="4b817-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4b817-129">-Confirm</span></span>
<span data-ttu-id="4b817-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b817-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b817-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b817-131">-WhatIf</span></span>
<span data-ttu-id="4b817-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4b817-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4b817-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4b817-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b817-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b817-134">CommonParameters</span></span>
<span data-ttu-id="4b817-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b817-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b817-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4b817-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b817-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4b817-137">INPUTS</span></span>

### <span data-ttu-id="4b817-138">System. String</span><span class="sxs-lookup"><span data-stu-id="4b817-138">System.String</span></span>

### <span data-ttu-id="4b817-139">Microsoft. Azure. PowerShell. cmdlets. StackEdge. Models. PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="4b817-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="4b817-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4b817-140">OUTPUTS</span></span>

### <span data-ttu-id="4b817-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4b817-141">System.Boolean</span></span>

## <span data-ttu-id="4b817-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4b817-142">NOTES</span></span>

## <span data-ttu-id="4b817-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4b817-143">RELATED LINKS</span></span>
