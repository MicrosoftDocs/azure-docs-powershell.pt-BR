---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstorageblobrestorepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobRestorePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobRestorePolicy.md
ms.openlocfilehash: 8e68400eeaedd6529ffc4069b36c6f73e25864f1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113936"
---
# <span data-ttu-id="955ea-101">Disable-AzStorageBlobRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="955ea-101">Disable-AzStorageBlobRestorePolicy</span></span>

## <span data-ttu-id="955ea-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="955ea-102">SYNOPSIS</span></span>
<span data-ttu-id="955ea-103">Desabilita a Política de Restauração de Blob em uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="955ea-103">Disables Blob Restore Policy on a Storage account.</span></span>

## <span data-ttu-id="955ea-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="955ea-104">SYNTAX</span></span>

### <span data-ttu-id="955ea-105">Nomeda Conta (Padrão)</span><span class="sxs-lookup"><span data-stu-id="955ea-105">AccountName (Default)</span></span>
```
Disable-AzStorageBlobRestorePolicy [-ResourceGroupName] <String> [-StorageAccountName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="955ea-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="955ea-106">AccountObject</span></span>
```
Disable-AzStorageBlobRestorePolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="955ea-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="955ea-107">BlobServicePropertiesResourceId</span></span>
```
Disable-AzStorageBlobRestorePolicy [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="955ea-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="955ea-108">DESCRIPTION</span></span>
<span data-ttu-id="955ea-109">O cmdlet **Disable-AzStorageBstorePolicy** desabilita a Política de Restauração de Blob para o serviço blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="955ea-109">The **Disable-AzStorageBlobRestorePolicy** cmdlet disables Blob Restore Policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="955ea-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="955ea-110">EXAMPLES</span></span>

### <span data-ttu-id="955ea-111">Exemplo 1: desabilita a Política de Restauração de Blob para o serviço blob de armazenamento do Azure em uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="955ea-111">Example 1: Disables Blob Restore Policy for the Azure Storage Blob service on a Storage account</span></span>
```powershell
PS C:\> Disable-AzStorageBlobRestorePolicy -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount"
```

<span data-ttu-id="955ea-112">Este comando desabilita a Política de Restauração de Blob para o serviço blob de armazenamento do Azure em uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="955ea-112">This command Disables Blob Restore Policy for the Azure Storage Blob service on a Storage account.</span></span>

## <span data-ttu-id="955ea-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="955ea-113">PARAMETERS</span></span>

### <span data-ttu-id="955ea-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="955ea-114">-DefaultProfile</span></span>
<span data-ttu-id="955ea-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="955ea-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="955ea-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="955ea-116">-PassThru</span></span>
<span data-ttu-id="955ea-117">Exibir ServiceProperties</span><span class="sxs-lookup"><span data-stu-id="955ea-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="955ea-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="955ea-118">-ResourceGroupName</span></span>
<span data-ttu-id="955ea-119">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="955ea-119">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="955ea-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="955ea-120">-ResourceId</span></span>
<span data-ttu-id="955ea-121">Inserir uma ID de Recurso de conta de armazenamento ou uma ID de recurso de propriedades do serviço Blob.</span><span class="sxs-lookup"><span data-stu-id="955ea-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="955ea-122">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="955ea-122">-StorageAccount</span></span>
<span data-ttu-id="955ea-123">Objeto de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="955ea-123">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="955ea-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="955ea-124">-StorageAccountName</span></span>
<span data-ttu-id="955ea-125">Nome da Conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="955ea-125">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="955ea-126">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="955ea-126">-Confirm</span></span>
<span data-ttu-id="955ea-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="955ea-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="955ea-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="955ea-128">-WhatIf</span></span>
<span data-ttu-id="955ea-129">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="955ea-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="955ea-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="955ea-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="955ea-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="955ea-131">CommonParameters</span></span>
<span data-ttu-id="955ea-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="955ea-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="955ea-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="955ea-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="955ea-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="955ea-134">INPUTS</span></span>

### <span data-ttu-id="955ea-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="955ea-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="955ea-136">System.String</span><span class="sxs-lookup"><span data-stu-id="955ea-136">System.String</span></span>

## <span data-ttu-id="955ea-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="955ea-137">OUTPUTS</span></span>

### <span data-ttu-id="955ea-138">Microsoft.Azure.Commands.Management.Storage.Models.PSRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="955ea-138">Microsoft.Azure.Commands.Management.Storage.Models.PSRestorePolicy</span></span>

## <span data-ttu-id="955ea-139">Notas</span><span class="sxs-lookup"><span data-stu-id="955ea-139">NOTES</span></span>

## <span data-ttu-id="955ea-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="955ea-140">RELATED LINKS</span></span>
