---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: C4E7ACDF-22FB-4D49-93B3-69E787B7E0CD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/restore-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultKey.md
ms.openlocfilehash: aee61173ee327d0c65f4cc04451fd64f51a79522
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602854"
---
# <span data-ttu-id="b31b0-101">Restore-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b31b0-101">Restore-AzureKeyVaultKey</span></span>

## <span data-ttu-id="b31b0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b31b0-102">SYNOPSIS</span></span>
<span data-ttu-id="b31b0-103">Cria uma chave em um cofre de chaves de uma chave com backup.</span><span class="sxs-lookup"><span data-stu-id="b31b0-103">Creates a key in a key vault from a backed-up key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b31b0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b31b0-104">SYNTAX</span></span>

### <span data-ttu-id="b31b0-105">ByVaultName (padrão)</span><span class="sxs-lookup"><span data-stu-id="b31b0-105">ByVaultName (Default)</span></span>
```
Restore-AzureKeyVaultKey [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b31b0-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b31b0-106">ByInputObject</span></span>
```
Restore-AzureKeyVaultKey [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b31b0-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b31b0-107">DESCRIPTION</span></span>
<span data-ttu-id="b31b0-108">O cmdlet **Restore-AzureKeyVaultKey** cria uma chave no cofre de chaves especificado.</span><span class="sxs-lookup"><span data-stu-id="b31b0-108">The **Restore-AzureKeyVaultKey** cmdlet creates a key in the specified key vault.</span></span>
<span data-ttu-id="b31b0-109">Essa chave é uma réplica da chave com backup no arquivo de entrada e tem o mesmo nome da chave original.</span><span class="sxs-lookup"><span data-stu-id="b31b0-109">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="b31b0-110">Se o cofre de chaves já tiver uma chave com o mesmo nome, esse cmdlet falha em vez de substituir a chave original.</span><span class="sxs-lookup"><span data-stu-id="b31b0-110">If the key vault already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="b31b0-111">Se o backup contiver várias versões de uma chave, todas as versões serão restauradas.</span><span class="sxs-lookup"><span data-stu-id="b31b0-111">If the backup contains multiple versions of a key, all versions are restored.</span></span>

<span data-ttu-id="b31b0-112">O cofre de chaves no qual você restaura a chave pode ser diferente do cofre de chaves do qual você tem o backup da chave.</span><span class="sxs-lookup"><span data-stu-id="b31b0-112">The key vault that you restore the key into can be different from the key vault that you backed up the key from.</span></span>
<span data-ttu-id="b31b0-113">No entanto, o cofre de chaves deve usar a mesma assinatura e estar em uma região do Azure na mesma Geografia (por exemplo, América do Norte).</span><span class="sxs-lookup"><span data-stu-id="b31b0-113">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="b31b0-114">Consulte a central de confiabilidade do Microsoft Azure ( https://azure.microsoft.com/support/trust-center/) para o mapeamento de regiões do Azure para regiões geográficas.</span><span class="sxs-lookup"><span data-stu-id="b31b0-114">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="b31b0-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b31b0-115">EXAMPLES</span></span>

### <span data-ttu-id="b31b0-116">Exemplo 1: restaurar uma chave de backup</span><span class="sxs-lookup"><span data-stu-id="b31b0-116">Example 1: Restore a backed-up key</span></span>
```
PS C:\>Restore-AzureKeyVaultKey -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="b31b0-117">Esse comando restaura uma chave, incluindo todas as suas versões, do arquivo de backup chamado backup. blob no cofre de chaves chamado MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="b31b0-117">This command restores a key, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="b31b0-118">OS</span><span class="sxs-lookup"><span data-stu-id="b31b0-118">PARAMETERS</span></span>

### <span data-ttu-id="b31b0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b31b0-119">-DefaultProfile</span></span>
<span data-ttu-id="b31b0-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b31b0-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b31b0-121">-InputFile</span><span class="sxs-lookup"><span data-stu-id="b31b0-121">-InputFile</span></span>
<span data-ttu-id="b31b0-122">Especifica o arquivo de entrada que contém o backup da chave a ser restaurada.</span><span class="sxs-lookup"><span data-stu-id="b31b0-122">Specifies the input file that contains the backup of the key to restore.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b31b0-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b31b0-123">-InputObject</span></span>
<span data-ttu-id="b31b0-124">Objeto do keyvault</span><span class="sxs-lookup"><span data-stu-id="b31b0-124">KeyVault object</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b31b0-125">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="b31b0-125">-VaultName</span></span>
<span data-ttu-id="b31b0-126">Especifica o nome do cofre de chaves no qual a chave será restaurada.</span><span class="sxs-lookup"><span data-stu-id="b31b0-126">Specifies the name of the key vault into which to restore the key.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b31b0-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b31b0-127">-Confirm</span></span>
<span data-ttu-id="b31b0-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b31b0-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b31b0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b31b0-129">-WhatIf</span></span>
<span data-ttu-id="b31b0-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b31b0-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b31b0-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b31b0-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b31b0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b31b0-132">CommonParameters</span></span>
<span data-ttu-id="b31b0-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b31b0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b31b0-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b31b0-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b31b0-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b31b0-135">INPUTS</span></span>

### <span data-ttu-id="b31b0-136">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="b31b0-136">None</span></span>
<span data-ttu-id="b31b0-137">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="b31b0-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b31b0-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b31b0-138">OUTPUTS</span></span>

### <span data-ttu-id="b31b0-139">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b31b0-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="b31b0-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b31b0-140">NOTES</span></span>

## <span data-ttu-id="b31b0-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b31b0-141">RELATED LINKS</span></span>

[<span data-ttu-id="b31b0-142">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b31b0-142">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="b31b0-143">Backup-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b31b0-143">Backup-AzureKeyVaultKey</span></span>](./Backup-AzureKeyVaultKey.md)

[<span data-ttu-id="b31b0-144">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b31b0-144">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="b31b0-145">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b31b0-145">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

