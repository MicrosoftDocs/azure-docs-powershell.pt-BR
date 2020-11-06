---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultKeyRemoval.md
ms.openlocfilehash: df29d88fbac1a8d2dc382522e24ff143cf075573
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440624"
---
# <span data-ttu-id="ba301-101">Undo-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="ba301-101">Undo-AzureKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="ba301-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ba301-102">SYNOPSIS</span></span>
<span data-ttu-id="ba301-103">Recupera uma chave excluída em um cofre de chaves para um estado ativo.</span><span class="sxs-lookup"><span data-stu-id="ba301-103">Recovers a deleted key in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba301-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ba301-104">SYNTAX</span></span>

```
Undo-AzureKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba301-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ba301-105">DESCRIPTION</span></span>
<span data-ttu-id="ba301-106">O cmdlet **Undo-AzureKeyVaultKeyRemoval** recuperará uma chave previamente excluída.</span><span class="sxs-lookup"><span data-stu-id="ba301-106">The **Undo-AzureKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="ba301-107">A chave recuperada estará ativa e poderá ser usada para todas as operações de chave normais.</span><span class="sxs-lookup"><span data-stu-id="ba301-107">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="ba301-108">O chamador precisa ter a permissão ' recuperar ' para executar essa operação.</span><span class="sxs-lookup"><span data-stu-id="ba301-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="ba301-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ba301-109">EXAMPLES</span></span>

### <span data-ttu-id="ba301-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ba301-110">Example 1</span></span>
```
PS C:\>Undo-AzureKeyVaultKeyRemoval -VaultName 'MyKeyVault' -Name 'MyKey'
```

<span data-ttu-id="ba301-111">Esse comando recuperará a chave ' MyKey ' que foi excluída anteriormente, em um estado ativo e utilizável.</span><span class="sxs-lookup"><span data-stu-id="ba301-111">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="ba301-112">OS</span><span class="sxs-lookup"><span data-stu-id="ba301-112">PARAMETERS</span></span>

### <span data-ttu-id="ba301-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="ba301-113">-Name</span></span>
<span data-ttu-id="ba301-114">Nome da chave.</span><span class="sxs-lookup"><span data-stu-id="ba301-114">Key name.</span></span>
<span data-ttu-id="ba301-115">O cmdlet constrói o FQDN de uma chave do nome do cofre, o ambiente selecionado no momento e o nome da chave.</span><span class="sxs-lookup"><span data-stu-id="ba301-115">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba301-116">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="ba301-116">-VaultName</span></span>
<span data-ttu-id="ba301-117">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="ba301-117">Vault name.</span></span>
<span data-ttu-id="ba301-118">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="ba301-118">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba301-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ba301-119">-Confirm</span></span>
<span data-ttu-id="ba301-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba301-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba301-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba301-121">-WhatIf</span></span>
<span data-ttu-id="ba301-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ba301-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba301-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ba301-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba301-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba301-124">-DefaultProfile</span></span>
<span data-ttu-id="ba301-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ba301-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba301-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba301-126">CommonParameters</span></span>
<span data-ttu-id="ba301-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba301-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba301-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba301-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba301-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ba301-129">INPUTS</span></span>

### <span data-ttu-id="ba301-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ba301-130">System.String</span></span>

## <span data-ttu-id="ba301-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ba301-131">OUTPUTS</span></span>

### <span data-ttu-id="ba301-132">Microsoft. Azure. Commands. keyvault. Models. keybundle</span><span class="sxs-lookup"><span data-stu-id="ba301-132">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="ba301-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ba301-133">NOTES</span></span>

## <span data-ttu-id="ba301-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ba301-134">RELATED LINKS</span></span>

[<span data-ttu-id="ba301-135">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ba301-135">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="ba301-136">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ba301-136">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="ba301-137">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ba301-137">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

