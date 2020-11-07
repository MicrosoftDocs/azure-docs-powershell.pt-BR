---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverkeyvaultcredentialconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
ms.openlocfilehash: d9f732a40b61687d7970fdf24f9f9f0f841b2cc7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776953"
---
# <span data-ttu-id="07200-101">New-AzVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="07200-101">New-AzVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="07200-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="07200-102">SYNOPSIS</span></span>
<span data-ttu-id="07200-103">Cria um objeto de configuração para a credencial do cofre de chaves do SQL Server em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="07200-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

## <span data-ttu-id="07200-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="07200-104">SYNTAX</span></span>

```
New-AzVMSqlServerKeyVaultCredentialConfig [-ResourceGroupName] <String> [-Enable]
 [-CredentialName <String>] [-AzureKeyVaultUrl <String>] [-ServicePrincipalName <String>]
 [-ServicePrincipalSecret <SecureString>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07200-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="07200-105">DESCRIPTION</span></span>

## <span data-ttu-id="07200-106">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="07200-106">EXAMPLES</span></span>

## <span data-ttu-id="07200-107">OS</span><span class="sxs-lookup"><span data-stu-id="07200-107">PARAMETERS</span></span>

### <span data-ttu-id="07200-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="07200-108">-AzureKeyVaultUrl</span></span>
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

### <span data-ttu-id="07200-109">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="07200-109">-CredentialName</span></span>
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

### <span data-ttu-id="07200-110">-Habilitar</span><span class="sxs-lookup"><span data-stu-id="07200-110">-Enable</span></span>
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

### <span data-ttu-id="07200-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07200-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="07200-112">-Serviceprincipalnamename</span><span class="sxs-lookup"><span data-stu-id="07200-112">-ServicePrincipalName</span></span>
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

### <span data-ttu-id="07200-113">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="07200-113">-ServicePrincipalSecret</span></span>
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

### <span data-ttu-id="07200-114">-Confirme</span><span class="sxs-lookup"><span data-stu-id="07200-114">-Confirm</span></span>
<span data-ttu-id="07200-115">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07200-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07200-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07200-116">-WhatIf</span></span>
<span data-ttu-id="07200-117">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="07200-117">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="07200-118">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="07200-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07200-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07200-119">CommonParameters</span></span>
<span data-ttu-id="07200-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07200-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07200-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07200-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07200-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="07200-122">INPUTS</span></span>

### <span data-ttu-id="07200-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="07200-123">None</span></span>
<span data-ttu-id="07200-124">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="07200-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="07200-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="07200-125">OUTPUTS</span></span>

### <span data-ttu-id="07200-126">Microsoft. Azure. Commands. COMPUTE. KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="07200-126">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="07200-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="07200-127">NOTES</span></span>

## <span data-ttu-id="07200-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="07200-128">RELATED LINKS</span></span>

