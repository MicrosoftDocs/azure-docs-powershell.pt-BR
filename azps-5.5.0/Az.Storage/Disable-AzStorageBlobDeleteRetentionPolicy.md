---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstorageblobdeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobDeleteRetentionPolicy.md
ms.openlocfilehash: f3891d30322a7c6577c14d43f7796a3242b53ecf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113937"
---
# <span data-ttu-id="75312-101">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="75312-101">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>

## <span data-ttu-id="75312-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="75312-102">SYNOPSIS</span></span>
<span data-ttu-id="75312-103">Desabilitar a política de retenção de exclusão do serviço Blob de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="75312-103">Disable delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="75312-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="75312-104">SYNTAX</span></span>

### <span data-ttu-id="75312-105">Nomeda Conta (Padrão)</span><span class="sxs-lookup"><span data-stu-id="75312-105">AccountName (Default)</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75312-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="75312-106">AccountObject</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75312-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="75312-107">BlobServicePropertiesResourceId</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75312-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="75312-108">DESCRIPTION</span></span>
<span data-ttu-id="75312-109">O cmdlet **Disable-AzStorageBleteRetentionPolicy** desabilita a política de retenção de exclusão do serviço blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="75312-109">The **Disable-AzStorageBlobDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="75312-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="75312-110">EXAMPLES</span></span>

### <span data-ttu-id="75312-111">Exemplo 1: Desabilitar a política de retenção de exclusão para o serviço Blob</span><span class="sxs-lookup"><span data-stu-id="75312-111">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzStorageBlobDeleteRetentionPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PassThru

Enabled Days
------- ----
  False
```

<span data-ttu-id="75312-112">Esse comando desabilita a política de retenção de exclusão do serviço Blob.</span><span class="sxs-lookup"><span data-stu-id="75312-112">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="75312-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="75312-113">PARAMETERS</span></span>

### <span data-ttu-id="75312-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75312-114">-DefaultProfile</span></span>
<span data-ttu-id="75312-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="75312-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75312-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="75312-116">-PassThru</span></span>
<span data-ttu-id="75312-117">Exibir ServiceProperties</span><span class="sxs-lookup"><span data-stu-id="75312-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="75312-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75312-118">-ResourceGroupName</span></span>
<span data-ttu-id="75312-119">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="75312-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="75312-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75312-120">-ResourceId</span></span>
<span data-ttu-id="75312-121">Inserir uma ID de Recurso de conta de armazenamento ou uma ID de recurso de propriedades do serviço Blob.</span><span class="sxs-lookup"><span data-stu-id="75312-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="75312-122">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="75312-122">-StorageAccount</span></span>
<span data-ttu-id="75312-123">Objeto de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="75312-123">Storage account object</span></span>

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

### <span data-ttu-id="75312-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="75312-124">-StorageAccountName</span></span>
<span data-ttu-id="75312-125">Nome da Conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="75312-125">Storage Account Name.</span></span>

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

### <span data-ttu-id="75312-126">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="75312-126">-Confirm</span></span>
<span data-ttu-id="75312-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75312-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75312-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75312-128">-WhatIf</span></span>
<span data-ttu-id="75312-129">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="75312-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75312-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="75312-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75312-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75312-131">CommonParameters</span></span>
<span data-ttu-id="75312-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75312-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75312-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75312-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75312-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="75312-134">INPUTS</span></span>

### <span data-ttu-id="75312-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="75312-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="75312-136">System.String</span><span class="sxs-lookup"><span data-stu-id="75312-136">System.String</span></span>

## <span data-ttu-id="75312-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="75312-137">OUTPUTS</span></span>

### <span data-ttu-id="75312-138">Microsoft.Azure.Commands.Management.Storage.Models.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="75312-138">Microsoft.Azure.Commands.Management.Storage.Models.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="75312-139">Notas</span><span class="sxs-lookup"><span data-stu-id="75312-139">NOTES</span></span>

## <span data-ttu-id="75312-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="75312-140">RELATED LINKS</span></span>
