---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverkeyvaultcredentialconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
ms.openlocfilehash: 50bf29524e4c16a7a7186a547505f4dcf7dac4e2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93948409"
---
# <span data-ttu-id="a43c9-101">New-AzVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="a43c9-101">New-AzVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="a43c9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a43c9-102">SYNOPSIS</span></span>
<span data-ttu-id="a43c9-103">Cria um objeto de configuração para a credencial do cofre de chaves do SQL Server em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a43c9-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

## <span data-ttu-id="a43c9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a43c9-104">SYNTAX</span></span>

```
New-AzVMSqlServerKeyVaultCredentialConfig [-ResourceGroupName] <String> [-Enable] [-CredentialName <String>]
 [-AzureKeyVaultUrl <String>] [-ServicePrincipalName <String>] [-ServicePrincipalSecret <SecureString>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a43c9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a43c9-105">DESCRIPTION</span></span>

## <span data-ttu-id="a43c9-106">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a43c9-106">EXAMPLES</span></span>

## <span data-ttu-id="a43c9-107">OS</span><span class="sxs-lookup"><span data-stu-id="a43c9-107">PARAMETERS</span></span>

### <span data-ttu-id="a43c9-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="a43c9-108">-AzureKeyVaultUrl</span></span>
<span data-ttu-id="a43c9-109">URL do serviço do cofre de chaves do Azure</span><span class="sxs-lookup"><span data-stu-id="a43c9-109">Azure Key Vault service URL</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a43c9-110">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="a43c9-110">-CredentialName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a43c9-111">-Habilitar</span><span class="sxs-lookup"><span data-stu-id="a43c9-111">-Enable</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a43c9-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a43c9-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="a43c9-113">-Serviceprincipalnamename</span><span class="sxs-lookup"><span data-stu-id="a43c9-113">-ServicePrincipalName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a43c9-114">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="a43c9-114">-ServicePrincipalSecret</span></span>
```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a43c9-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a43c9-115">-Confirm</span></span>
<span data-ttu-id="a43c9-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a43c9-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a43c9-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a43c9-117">-WhatIf</span></span>
<span data-ttu-id="a43c9-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a43c9-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a43c9-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a43c9-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a43c9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a43c9-120">CommonParameters</span></span>
<span data-ttu-id="a43c9-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a43c9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a43c9-122">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a43c9-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a43c9-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a43c9-123">INPUTS</span></span>

### <span data-ttu-id="a43c9-124">System. String</span><span class="sxs-lookup"><span data-stu-id="a43c9-124">System.String</span></span>

### <span data-ttu-id="a43c9-125">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a43c9-125">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="a43c9-126">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="a43c9-126">System.Security.SecureString</span></span>

## <span data-ttu-id="a43c9-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a43c9-127">OUTPUTS</span></span>

### <span data-ttu-id="a43c9-128">Microsoft. Azure. Commands. COMPUTE. KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="a43c9-128">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="a43c9-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a43c9-129">NOTES</span></span>

## <span data-ttu-id="a43c9-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a43c9-130">RELATED LINKS</span></span>
