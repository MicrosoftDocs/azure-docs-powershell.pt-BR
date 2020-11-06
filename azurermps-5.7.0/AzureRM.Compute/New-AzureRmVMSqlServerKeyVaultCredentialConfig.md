---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerKeyVaultCredentialConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerKeyVaultCredentialConfig.md
ms.openlocfilehash: 4e252001d1459c52a35b766d34c91050df62073d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429871"
---
# <span data-ttu-id="ff54e-101">New-AzureVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="ff54e-101">New-AzureVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="ff54e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ff54e-102">SYNOPSIS</span></span>
<span data-ttu-id="ff54e-103">Cria um objeto de configuração para a credencial do cofre de chaves do SQL Server em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ff54e-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff54e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ff54e-104">SYNTAX</span></span>

```
New-AzureVMSqlServerKeyVaultCredentialConfig [-ResourceGroupName] <String> [-Enable] [-CredentialName <String>]
 [-AzureKeyVaultUrl <String>] [-ServicePrincipalName <String>] [-ServicePrincipalSecret <SecureString>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff54e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ff54e-105">DESCRIPTION</span></span>

## <span data-ttu-id="ff54e-106">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ff54e-106">EXAMPLES</span></span>

## <span data-ttu-id="ff54e-107">OS</span><span class="sxs-lookup"><span data-stu-id="ff54e-107">PARAMETERS</span></span>

### <span data-ttu-id="ff54e-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="ff54e-108">-AzureKeyVaultUrl</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff54e-109">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="ff54e-109">-CredentialName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff54e-110">-Habilitar</span><span class="sxs-lookup"><span data-stu-id="ff54e-110">-Enable</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff54e-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff54e-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="ff54e-112">-Serviceprincipalnamename</span><span class="sxs-lookup"><span data-stu-id="ff54e-112">-ServicePrincipalName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff54e-113">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="ff54e-113">-ServicePrincipalSecret</span></span>
```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff54e-114">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ff54e-114">-Confirm</span></span>
<span data-ttu-id="ff54e-115">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff54e-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff54e-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff54e-116">-WhatIf</span></span>
<span data-ttu-id="ff54e-117">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ff54e-117">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="ff54e-118">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ff54e-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff54e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff54e-119">CommonParameters</span></span>
<span data-ttu-id="ff54e-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff54e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff54e-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff54e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff54e-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ff54e-122">INPUTS</span></span>

### <span data-ttu-id="ff54e-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="ff54e-123">None</span></span>
<span data-ttu-id="ff54e-124">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="ff54e-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ff54e-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ff54e-125">OUTPUTS</span></span>

## <span data-ttu-id="ff54e-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ff54e-126">NOTES</span></span>

## <span data-ttu-id="ff54e-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ff54e-127">RELATED LINKS</span></span>

