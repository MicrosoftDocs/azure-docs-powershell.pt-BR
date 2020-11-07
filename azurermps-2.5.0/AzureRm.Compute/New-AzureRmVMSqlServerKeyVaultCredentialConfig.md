---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmsqlserverkeyvaultcredentialconfig
schema: 2.0.0
ms.openlocfilehash: ee627065d1d6be8037d1a9b054ec6452b9becb41
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786166"
---
# <span data-ttu-id="75ebf-101">New-AzureRmVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="75ebf-101">New-AzureRmVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="75ebf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="75ebf-102">SYNOPSIS</span></span>
<span data-ttu-id="75ebf-103">Cria um objeto de configuração para a credencial do cofre de chaves do SQL Server em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="75ebf-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75ebf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="75ebf-104">SYNTAX</span></span>

```
New-AzureRmVMSqlServerKeyVaultCredentialConfig [-ResourceGroupName] <String> [-Enable]
 [-CredentialName <String>] [-AzureKeyVaultUrl <String>] [-ServicePrincipalName <String>]
 [-ServicePrincipalSecret <SecureString>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75ebf-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="75ebf-105">DESCRIPTION</span></span>

## <span data-ttu-id="75ebf-106">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="75ebf-106">EXAMPLES</span></span>

## <span data-ttu-id="75ebf-107">OS</span><span class="sxs-lookup"><span data-stu-id="75ebf-107">PARAMETERS</span></span>

### <span data-ttu-id="75ebf-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="75ebf-108">-AzureKeyVaultUrl</span></span>
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

### <span data-ttu-id="75ebf-109">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="75ebf-109">-CredentialName</span></span>
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

### <span data-ttu-id="75ebf-110">-Habilitar</span><span class="sxs-lookup"><span data-stu-id="75ebf-110">-Enable</span></span>
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

### <span data-ttu-id="75ebf-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75ebf-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="75ebf-112">-Serviceprincipalnamename</span><span class="sxs-lookup"><span data-stu-id="75ebf-112">-ServicePrincipalName</span></span>
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

### <span data-ttu-id="75ebf-113">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="75ebf-113">-ServicePrincipalSecret</span></span>
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

### <span data-ttu-id="75ebf-114">-Confirme</span><span class="sxs-lookup"><span data-stu-id="75ebf-114">-Confirm</span></span>
<span data-ttu-id="75ebf-115">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75ebf-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75ebf-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75ebf-116">-WhatIf</span></span>
<span data-ttu-id="75ebf-117">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="75ebf-117">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="75ebf-118">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="75ebf-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75ebf-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75ebf-119">CommonParameters</span></span>
<span data-ttu-id="75ebf-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75ebf-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75ebf-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75ebf-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75ebf-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="75ebf-122">INPUTS</span></span>

### <span data-ttu-id="75ebf-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="75ebf-123">None</span></span>
<span data-ttu-id="75ebf-124">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="75ebf-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="75ebf-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="75ebf-125">OUTPUTS</span></span>

### <span data-ttu-id="75ebf-126">Microsoft. Azure. Commands. COMPUTE. KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="75ebf-126">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="75ebf-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="75ebf-127">NOTES</span></span>

## <span data-ttu-id="75ebf-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="75ebf-128">RELATED LINKS</span></span>

