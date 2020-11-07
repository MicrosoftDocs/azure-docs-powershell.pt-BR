---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 70DB088D-4AF5-406B-8D66-118A0F766041
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/restore-AzKeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Restore-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Restore-AzKeyVaultSecret.md
ms.openlocfilehash: 4691d37532db3dd8e629bf1daad2654558a31de3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776661"
---
# <span data-ttu-id="2c8b6-101">Restore-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="2c8b6-101">Restore-AzKeyVaultSecret</span></span>

## <span data-ttu-id="2c8b6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2c8b6-102">SYNOPSIS</span></span>
<span data-ttu-id="2c8b6-103">Cria um segredo em um cofre de chaves a partir de um segredo em backup.</span><span class="sxs-lookup"><span data-stu-id="2c8b6-103">Creates a secret in a key vault from a backed-up secret.</span></span>

## <span data-ttu-id="2c8b6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2c8b6-104">SYNTAX</span></span>

```
Restore-AzKeyVaultSecret [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c8b6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2c8b6-105">DESCRIPTION</span></span>
<span data-ttu-id="2c8b6-106">O cmdlet **Restore-AzKeyVaultSecret** cria um segredo no cofre de chaves especificado.</span><span class="sxs-lookup"><span data-stu-id="2c8b6-106">The **Restore-AzKeyVaultSecret** cmdlet creates a secret in the specified key vault.</span></span>
<span data-ttu-id="2c8b6-107">Esse segredo é uma réplica do segredo em backup no arquivo de entrada e tem o mesmo nome que o segredo original.</span><span class="sxs-lookup"><span data-stu-id="2c8b6-107">This secret is a replica of the backed-up secret in the input file and has the same name as the original secret.</span></span>
<span data-ttu-id="2c8b6-108">Se o cofre de chaves já tem um segredo com o mesmo nome, esse cmdlet falha em vez de substituir o segredo original.</span><span class="sxs-lookup"><span data-stu-id="2c8b6-108">If the key vault already has a secret by the same name, this cmdlet fails instead of overwriting the original secret.</span></span>
<span data-ttu-id="2c8b6-109">Se o backup contiver várias versões de um segredo, todas as versões serão restauradas.</span><span class="sxs-lookup"><span data-stu-id="2c8b6-109">If the backup contains multiple versions of a secret, all versions are restored.</span></span>

<span data-ttu-id="2c8b6-110">O cofre de chaves no qual você restaura o segredo pode ser diferente do cofre de chaves do qual você está fazendo o backup do segredo.</span><span class="sxs-lookup"><span data-stu-id="2c8b6-110">The key vault that you restore the secret into can be different from the key vault that you backed up the secret from.</span></span>
<span data-ttu-id="2c8b6-111">No entanto, o cofre de chaves deve usar a mesma assinatura e estar em uma região do Azure na mesma Geografia (por exemplo, América do Norte).</span><span class="sxs-lookup"><span data-stu-id="2c8b6-111">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="2c8b6-112">Consulte a central de confiabilidade do Microsoft Azure ( https://azure.microsoft.com/support/trust-center/) para o mapeamento de regiões do Azure para regiões geográficas.</span><span class="sxs-lookup"><span data-stu-id="2c8b6-112">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="2c8b6-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2c8b6-113">EXAMPLES</span></span>

### <span data-ttu-id="2c8b6-114">Exemplo 1: restaurar um segredo em backup</span><span class="sxs-lookup"><span data-stu-id="2c8b6-114">Example 1: Restore a backed-up secret</span></span>
```
PS C:\>Restore-AzKeyVaultSecret -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="2c8b6-115">Esse comando restaura um segredo, incluindo todas as suas versões, do arquivo de backup chamado backup. blob no cofre de chaves chamado MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="2c8b6-115">This command restores a secret, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="2c8b6-116">OS</span><span class="sxs-lookup"><span data-stu-id="2c8b6-116">PARAMETERS</span></span>

### <span data-ttu-id="2c8b6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c8b6-117">-DefaultProfile</span></span>
<span data-ttu-id="2c8b6-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="2c8b6-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2c8b6-119">-InputFile</span><span class="sxs-lookup"><span data-stu-id="2c8b6-119">-InputFile</span></span>
<span data-ttu-id="2c8b6-120">Especifica o arquivo de entrada que contém o backup do segredo a ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="2c8b6-120">Specifies the input file that contains the backup of the secret to restore.</span></span>

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

### <span data-ttu-id="2c8b6-121">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="2c8b6-121">-VaultName</span></span>
<span data-ttu-id="2c8b6-122">Especifica o nome do cofre de chaves no qual você deseja restaurar o segredo.</span><span class="sxs-lookup"><span data-stu-id="2c8b6-122">Specifies the name of the key vault into which to restore the secret.</span></span>

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

### <span data-ttu-id="2c8b6-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2c8b6-123">-Confirm</span></span>
<span data-ttu-id="2c8b6-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c8b6-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c8b6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c8b6-125">-WhatIf</span></span>
<span data-ttu-id="2c8b6-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2c8b6-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c8b6-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2c8b6-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c8b6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c8b6-128">CommonParameters</span></span>
<span data-ttu-id="2c8b6-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c8b6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c8b6-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c8b6-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c8b6-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2c8b6-131">INPUTS</span></span>

### <span data-ttu-id="2c8b6-132">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="2c8b6-132">None</span></span>
<span data-ttu-id="2c8b6-133">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="2c8b6-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2c8b6-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2c8b6-134">OUTPUTS</span></span>

### <span data-ttu-id="2c8b6-135">Microsoft. Azure. Commands. keyvault. Models. Secret</span><span class="sxs-lookup"><span data-stu-id="2c8b6-135">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="2c8b6-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2c8b6-136">NOTES</span></span>

## <span data-ttu-id="2c8b6-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2c8b6-137">RELATED LINKS</span></span>

[<span data-ttu-id="2c8b6-138">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="2c8b6-138">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="2c8b6-139">Backup-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="2c8b6-139">Backup-AzKeyVaultSecret</span></span>](./Backup-AzKeyVaultSecret.md)

[<span data-ttu-id="2c8b6-140">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="2c8b6-140">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="2c8b6-141">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="2c8b6-141">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

