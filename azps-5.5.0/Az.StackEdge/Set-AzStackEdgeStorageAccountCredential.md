---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: 89e727b836f28ac1972bcf15e872e2860a8a6672
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110886"
---
# <span data-ttu-id="fb701-101">Set-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="fb701-101">Set-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="fb701-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fb701-102">SYNOPSIS</span></span>
<span data-ttu-id="fb701-103">Define a credencial da conta de armazenamento para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fb701-103">Sets the storage account credential for a device.</span></span>

## <span data-ttu-id="fb701-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fb701-104">SYNTAX</span></span>

### <span data-ttu-id="fb701-105">SetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="fb701-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb701-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb701-106">SetByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeStorageAccountCredential -ResourceId <String> -StorageAccountAccessKey <SecureString>
 -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fb701-107">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb701-107">SetByParentObjectParameterSet</span></span>
```
Set-AzStackEdgeStorageAccountCredential -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSStackEdgeStorageAccountCredential>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb701-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="fb701-108">DESCRIPTION</span></span>
<span data-ttu-id="fb701-109">O cmdlet **Set-AzSt stackEdgeStorageAccountCredential** atualiza a credencial da conta de armazenamento correspondente a uma conta de armazenamento no dispositivo Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="fb701-109">The **Set-AzStackEdgeStorageAccountCredential** cmdlet updates the storage account credential corresponding to a storage account on the Stack Edge device.</span></span>

## <span data-ttu-id="fb701-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fb701-110">EXAMPLES</span></span>

### <span data-ttu-id="fb701-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fb701-111">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAcountCredentialName
 -StorageAccountName storageaccountname -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                        StorageAccount      SslStatus  ResourceGroupName
--------------------------- ------------------- ---------- ---------------------
storageAcountCredentialName storageaccountname  Enabled    resourceGroupName
```

<span data-ttu-id="fb701-112">Ajuda a girar as teclas de acesso para uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="fb701-112">Helps in rotating access keys for a storage account</span></span>

## <span data-ttu-id="fb701-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fb701-113">PARAMETERS</span></span>

### <span data-ttu-id="fb701-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fb701-114">-AsJob</span></span>
<span data-ttu-id="fb701-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="fb701-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fb701-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb701-116">-DefaultProfile</span></span>
<span data-ttu-id="fb701-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fb701-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb701-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="fb701-118">-DeviceName</span></span>
<span data-ttu-id="fb701-119">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="fb701-119">Device Name</span></span>

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

### <span data-ttu-id="fb701-120">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="fb701-120">-EncryptionKey</span></span>
<span data-ttu-id="fb701-121">Chave de criptografia do dispositivo Edge</span><span class="sxs-lookup"><span data-stu-id="fb701-121">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="fb701-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb701-122">-InputObject</span></span>
<span data-ttu-id="fb701-123">Objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="fb701-123">Input Object</span></span>

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

### <span data-ttu-id="fb701-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="fb701-124">-Name</span></span>
<span data-ttu-id="fb701-125">Nome da conta de armazenamento a ser usada</span><span class="sxs-lookup"><span data-stu-id="fb701-125">Name of the storage account to be used</span></span>

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

### <span data-ttu-id="fb701-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb701-126">-ResourceGroupName</span></span>
<span data-ttu-id="fb701-127">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="fb701-127">Resource Group Name</span></span>

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

### <span data-ttu-id="fb701-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb701-128">-ResourceId</span></span>
<span data-ttu-id="fb701-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb701-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="fb701-130">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="fb701-130">-StorageAccountAccessKey</span></span>
<span data-ttu-id="fb701-131">fornecer chave de acesso à conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="fb701-131">provide storage account access key</span></span>

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

### <span data-ttu-id="fb701-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="fb701-132">-Confirm</span></span>
<span data-ttu-id="fb701-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb701-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb701-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb701-134">-WhatIf</span></span>
<span data-ttu-id="fb701-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="fb701-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fb701-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fb701-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb701-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb701-137">CommonParameters</span></span>
<span data-ttu-id="fb701-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb701-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb701-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fb701-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb701-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="fb701-140">INPUTS</span></span>

### <span data-ttu-id="fb701-141">System.String</span><span class="sxs-lookup"><span data-stu-id="fb701-141">System.String</span></span>

### <span data-ttu-id="fb701-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSSt stackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="fb701-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="fb701-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="fb701-143">OUTPUTS</span></span>

### <span data-ttu-id="fb701-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSSt stackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="fb701-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="fb701-145">Notas</span><span class="sxs-lookup"><span data-stu-id="fb701-145">NOTES</span></span>

## <span data-ttu-id="fb701-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fb701-146">RELATED LINKS</span></span>
