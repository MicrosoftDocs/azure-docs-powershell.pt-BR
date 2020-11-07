---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: C4E7ACDF-22FB-4D49-93B3-69E787B7E0CD
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/restore-AzKeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Restore-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Restore-AzKeyVaultKey.md
ms.openlocfilehash: 5d090bae05e3d931fbf41b656ea66409d1297e8f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776664"
---
# <span data-ttu-id="a2b25-101">Restore-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a2b25-101">Restore-AzKeyVaultKey</span></span>

## <span data-ttu-id="a2b25-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a2b25-102">SYNOPSIS</span></span>
<span data-ttu-id="a2b25-103">Cria uma chave em um cofre de chaves de uma chave com backup.</span><span class="sxs-lookup"><span data-stu-id="a2b25-103">Creates a key in a key vault from a backed-up key.</span></span>

## <span data-ttu-id="a2b25-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a2b25-104">SYNTAX</span></span>

```
Restore-AzKeyVaultKey [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2b25-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a2b25-105">DESCRIPTION</span></span>
<span data-ttu-id="a2b25-106">O cmdlet **Restore-AzKeyVaultKey** cria uma chave no cofre de chaves especificado.</span><span class="sxs-lookup"><span data-stu-id="a2b25-106">The **Restore-AzKeyVaultKey** cmdlet creates a key in the specified key vault.</span></span>
<span data-ttu-id="a2b25-107">Essa chave é uma réplica da chave com backup no arquivo de entrada e tem o mesmo nome da chave original.</span><span class="sxs-lookup"><span data-stu-id="a2b25-107">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="a2b25-108">Se o cofre de chaves já tiver uma chave com o mesmo nome, esse cmdlet falha em vez de substituir a chave original.</span><span class="sxs-lookup"><span data-stu-id="a2b25-108">If the key vault already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="a2b25-109">Se o backup contiver várias versões de uma chave, todas as versões serão restauradas.</span><span class="sxs-lookup"><span data-stu-id="a2b25-109">If the backup contains multiple versions of a key, all versions are restored.</span></span>

<span data-ttu-id="a2b25-110">O cofre de chaves no qual você restaura a chave pode ser diferente do cofre de chaves do qual você tem o backup da chave.</span><span class="sxs-lookup"><span data-stu-id="a2b25-110">The key vault that you restore the key into can be different from the key vault that you backed up the key from.</span></span>
<span data-ttu-id="a2b25-111">No entanto, o cofre de chaves deve usar a mesma assinatura e estar em uma região do Azure na mesma Geografia (por exemplo, América do Norte).</span><span class="sxs-lookup"><span data-stu-id="a2b25-111">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="a2b25-112">Consulte a central de confiabilidade do Microsoft Azure ( https://azure.microsoft.com/support/trust-center/) para o mapeamento de regiões do Azure para regiões geográficas.</span><span class="sxs-lookup"><span data-stu-id="a2b25-112">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="a2b25-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a2b25-113">EXAMPLES</span></span>

### <span data-ttu-id="a2b25-114">Exemplo 1: restaurar uma chave de backup</span><span class="sxs-lookup"><span data-stu-id="a2b25-114">Example 1: Restore a backed-up key</span></span>
```
PS C:\>Restore-AzKeyVaultKey -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="a2b25-115">Esse comando restaura uma chave, incluindo todas as suas versões, do arquivo de backup chamado backup. blob no cofre de chaves chamado MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="a2b25-115">This command restores a key, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="a2b25-116">OS</span><span class="sxs-lookup"><span data-stu-id="a2b25-116">PARAMETERS</span></span>

### <span data-ttu-id="a2b25-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2b25-117">-DefaultProfile</span></span>
<span data-ttu-id="a2b25-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a2b25-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2b25-119">-InputFile</span><span class="sxs-lookup"><span data-stu-id="a2b25-119">-InputFile</span></span>
<span data-ttu-id="a2b25-120">Especifica o arquivo de entrada que contém o backup da chave a ser restaurada.</span><span class="sxs-lookup"><span data-stu-id="a2b25-120">Specifies the input file that contains the backup of the key to restore.</span></span>

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

### <span data-ttu-id="a2b25-121">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="a2b25-121">-VaultName</span></span>
<span data-ttu-id="a2b25-122">Especifica o nome do cofre de chaves no qual a chave será restaurada.</span><span class="sxs-lookup"><span data-stu-id="a2b25-122">Specifies the name of the key vault into which to restore the key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2b25-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a2b25-123">-Confirm</span></span>
<span data-ttu-id="a2b25-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2b25-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2b25-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2b25-125">-WhatIf</span></span>
<span data-ttu-id="a2b25-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a2b25-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2b25-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a2b25-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2b25-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2b25-128">CommonParameters</span></span>
<span data-ttu-id="a2b25-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2b25-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2b25-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2b25-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2b25-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a2b25-131">INPUTS</span></span>

### <span data-ttu-id="a2b25-132">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a2b25-132">None</span></span>
<span data-ttu-id="a2b25-133">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="a2b25-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a2b25-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a2b25-134">OUTPUTS</span></span>

### <span data-ttu-id="a2b25-135">Microsoft. Azure. Commands. keyvault. Models. keybundle</span><span class="sxs-lookup"><span data-stu-id="a2b25-135">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="a2b25-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a2b25-136">NOTES</span></span>

## <span data-ttu-id="a2b25-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a2b25-137">RELATED LINKS</span></span>

[<span data-ttu-id="a2b25-138">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a2b25-138">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="a2b25-139">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a2b25-139">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="a2b25-140">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a2b25-140">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="a2b25-141">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a2b25-141">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

