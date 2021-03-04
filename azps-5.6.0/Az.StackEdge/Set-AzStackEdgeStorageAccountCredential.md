---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/set-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: 089979d2b571b7141758baf3f8d103a5a322bc28
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890933"
---
# <span data-ttu-id="6d1f0-101">Set-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="6d1f0-101">Set-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="6d1f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d1f0-102">SYNOPSIS</span></span>
<span data-ttu-id="6d1f0-103">Define a credencial da conta de armazenamento para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6d1f0-103">Sets the storage account credential for a device.</span></span>

## <span data-ttu-id="6d1f0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6d1f0-104">SYNTAX</span></span>

### <span data-ttu-id="6d1f0-105">SetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6d1f0-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d1f0-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d1f0-106">SetByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeStorageAccountCredential -ResourceId <String> -StorageAccountAccessKey <SecureString>
 -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6d1f0-107">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d1f0-107">SetByParentObjectParameterSet</span></span>
```
Set-AzStackEdgeStorageAccountCredential -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSStackEdgeStorageAccountCredential>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d1f0-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6d1f0-108">DESCRIPTION</span></span>
<span data-ttu-id="6d1f0-109">O cmdlet **Set-AzStackEdgeStorageAccountCredential** atualiza a credencial da conta de armazenamento correspondente a uma conta de armazenamento no dispositivo de Borda de Pilha.</span><span class="sxs-lookup"><span data-stu-id="6d1f0-109">The **Set-AzStackEdgeStorageAccountCredential** cmdlet updates the storage account credential corresponding to a storage account on the Stack Edge device.</span></span>

## <span data-ttu-id="6d1f0-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6d1f0-110">EXAMPLES</span></span>

### <span data-ttu-id="6d1f0-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6d1f0-111">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAcountCredentialName
 -StorageAccountName storageaccountname -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                        StorageAccount      SslStatus  ResourceGroupName
--------------------------- ------------------- ---------- ---------------------
storageAcountCredentialName storageaccountname  Enabled    resourceGroupName
```

<span data-ttu-id="6d1f0-112">Ajuda na rotação de chaves de acesso para uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="6d1f0-112">Helps in rotating access keys for a storage account</span></span>

## <span data-ttu-id="6d1f0-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6d1f0-113">PARAMETERS</span></span>

### <span data-ttu-id="6d1f0-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d1f0-114">-AsJob</span></span>
<span data-ttu-id="6d1f0-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="6d1f0-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6d1f0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d1f0-116">-DefaultProfile</span></span>
<span data-ttu-id="6d1f0-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6d1f0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d1f0-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="6d1f0-118">-DeviceName</span></span>
<span data-ttu-id="6d1f0-119">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="6d1f0-119">Device Name</span></span>

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

### <span data-ttu-id="6d1f0-120">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="6d1f0-120">-EncryptionKey</span></span>
<span data-ttu-id="6d1f0-121">Chave de criptografia do dispositivo Edge</span><span class="sxs-lookup"><span data-stu-id="6d1f0-121">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="6d1f0-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d1f0-122">-InputObject</span></span>
<span data-ttu-id="6d1f0-123">Objeto Input</span><span class="sxs-lookup"><span data-stu-id="6d1f0-123">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential
Parameter Sets: SetByParentObjectParameterSet
Aliases: StorageAccountCredential

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d1f0-124">-Name</span><span class="sxs-lookup"><span data-stu-id="6d1f0-124">-Name</span></span>
<span data-ttu-id="6d1f0-125">Nome da conta de armazenamento a ser usada</span><span class="sxs-lookup"><span data-stu-id="6d1f0-125">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: StorageAccountCredentialName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d1f0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d1f0-126">-ResourceGroupName</span></span>
<span data-ttu-id="6d1f0-127">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="6d1f0-127">Resource Group Name</span></span>

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

### <span data-ttu-id="6d1f0-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d1f0-128">-ResourceId</span></span>
<span data-ttu-id="6d1f0-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d1f0-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="6d1f0-130">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="6d1f0-130">-StorageAccountAccessKey</span></span>
<span data-ttu-id="6d1f0-131">fornecer chave de acesso à conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="6d1f0-131">provide storage account access key</span></span>

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

### <span data-ttu-id="6d1f0-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6d1f0-132">-Confirm</span></span>
<span data-ttu-id="6d1f0-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d1f0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d1f0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d1f0-134">-WhatIf</span></span>
<span data-ttu-id="6d1f0-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6d1f0-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6d1f0-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6d1f0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d1f0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d1f0-137">CommonParameters</span></span>
<span data-ttu-id="6d1f0-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d1f0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d1f0-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6d1f0-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d1f0-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6d1f0-140">INPUTS</span></span>

### <span data-ttu-id="6d1f0-141">System.String</span><span class="sxs-lookup"><span data-stu-id="6d1f0-141">System.String</span></span>

### <span data-ttu-id="6d1f0-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="6d1f0-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="6d1f0-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6d1f0-143">OUTPUTS</span></span>

### <span data-ttu-id="6d1f0-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="6d1f0-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="6d1f0-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="6d1f0-145">NOTES</span></span>

## <span data-ttu-id="6d1f0-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6d1f0-146">RELATED LINKS</span></span>
