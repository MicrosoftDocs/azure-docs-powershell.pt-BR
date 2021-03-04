---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/set-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: 214b43148020b2884013a45f26b4a03cd4ea3736
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887796"
---
# <span data-ttu-id="14679-101">Set-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="14679-101">Set-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="14679-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14679-102">SYNOPSIS</span></span>
<span data-ttu-id="14679-103">Define a credencial da conta de armazenamento para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="14679-103">Sets the storage account credential for a device.</span></span>

## <span data-ttu-id="14679-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="14679-104">SYNTAX</span></span>

### <span data-ttu-id="14679-105">SetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="14679-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14679-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="14679-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeStorageAccountCredential -ResourceId <String> -StorageAccountAccessKey <SecureString>
 -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="14679-107">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="14679-107">SetByParentObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeStorageAccountCredential -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSDataBoxEdgeStorageAccountCredential>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14679-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="14679-108">DESCRIPTION</span></span>
<span data-ttu-id="14679-109">O cmdlet **Set-AzDataBoxEdgeStorageAccountCredential** atualiza a credencial da conta de armazenamento correspondente a uma conta de armazenamento no dispositivo de Borda da Caixa de Dados.</span><span class="sxs-lookup"><span data-stu-id="14679-109">The **Set-AzDataBoxEdgeStorageAccountCredential** cmdlet updates the storage account credential corresponding to a storage account on the Data Box Edge device.</span></span>

## <span data-ttu-id="14679-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="14679-110">EXAMPLES</span></span>

### <span data-ttu-id="14679-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="14679-111">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAcountCredentialName
 -StorageAccountName storageaccountname -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                        StorageAccount      SslStatus  ResourceGroupName
--------------------------- ------------------- ---------- ---------------------
storageAcountCredentialName storageaccountname  Enabled    resourceGroupName
```

<span data-ttu-id="14679-112">Ajuda na rotação de chaves de acesso para uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="14679-112">Helps in rotating access keys for a storage account</span></span>

## <span data-ttu-id="14679-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="14679-113">PARAMETERS</span></span>

### <span data-ttu-id="14679-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="14679-114">-AsJob</span></span>
<span data-ttu-id="14679-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="14679-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="14679-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14679-116">-DefaultProfile</span></span>
<span data-ttu-id="14679-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="14679-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14679-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="14679-118">-DeviceName</span></span>
<span data-ttu-id="14679-119">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="14679-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14679-120">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="14679-120">-EncryptionKey</span></span>
<span data-ttu-id="14679-121">Chave de criptografia do dispositivo Edge</span><span class="sxs-lookup"><span data-stu-id="14679-121">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14679-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14679-122">-InputObject</span></span>
<span data-ttu-id="14679-123">Objeto Input</span><span class="sxs-lookup"><span data-stu-id="14679-123">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential
Parameter Sets: SetByParentObjectParameterSet
Aliases: StorageAccountCredential

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14679-124">-Name</span><span class="sxs-lookup"><span data-stu-id="14679-124">-Name</span></span>
<span data-ttu-id="14679-125">Nome da conta de armazenamento a ser usada</span><span class="sxs-lookup"><span data-stu-id="14679-125">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: StorageAccountName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14679-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14679-126">-ResourceGroupName</span></span>
<span data-ttu-id="14679-127">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="14679-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14679-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14679-128">-ResourceId</span></span>
<span data-ttu-id="14679-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="14679-129">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14679-130">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="14679-130">-StorageAccountAccessKey</span></span>
<span data-ttu-id="14679-131">fornecer chave de acesso à conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="14679-131">provide storage account access key</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14679-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="14679-132">-Confirm</span></span>
<span data-ttu-id="14679-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14679-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14679-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14679-134">-WhatIf</span></span>
<span data-ttu-id="14679-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="14679-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="14679-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="14679-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14679-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14679-137">CommonParameters</span></span>
<span data-ttu-id="14679-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14679-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14679-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="14679-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14679-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="14679-140">INPUTS</span></span>

### <span data-ttu-id="14679-141">System.String</span><span class="sxs-lookup"><span data-stu-id="14679-141">System.String</span></span>

### <span data-ttu-id="14679-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="14679-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="14679-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="14679-143">OUTPUTS</span></span>

### <span data-ttu-id="14679-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="14679-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="14679-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="14679-145">NOTES</span></span>

## <span data-ttu-id="14679-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="14679-146">RELATED LINKS</span></span>
